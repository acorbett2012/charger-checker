/**
 * Created by ujad on 5/31/2018.
 */
angular.module("Charger.app", [])

    .filter('TrueFalseToAvailableUnavailable', function() {
        return function(input) {
            input = input || '';
            if (input == 'Loading'){
                out = 'Loading';
                return out;
            }
            var out = '';
            if (input == false) {
                out = 'NOT Available'
            } else {
                out = 'Available'
            }
            return out;
        };
    })

    .controller("ChargerController", function ($scope, $http) {
        var self = this;
        $scope.chargerStatuses = [];
        $scope.chargerStatus0 = 'Loading';
        $scope.chargerStatus1 = 'Loading';
        $scope.checkCount = 0;
        $scope.checkDate = new Date();

        var loopCheck = function () {
            $scope.checkCount++;
            $http({
                method: 'POST',
                url: 'https://cors-anywhere.herokuapp.com/https://network.semaconnect.com/get_data.php',
                headers: {'Content-Type': 'application/x-www-form-urlencoded'},
                data: 'action=mapLocationDetails&div_id=1499&user_id=35282'
            }).success(function (response) {
                var stations = response.aaData.stations;
                for(var x = 0; x<stations.length; x++) {
                    if (stations[x].status == "Available") {
                        if($scope.chargerStatuses[x]){
                            if ($scope.chargerStatuses[x].stationAvailable === false) {
                                alert('Station ' + x + ' Is now available' + new Date());
                            }
                        }
                        $scope.chargerStatuses[x] = {stationNumber: x , stationAvailable: true}
                    } else {
                        $scope.chargerStatuses[x] = {stationNumber: x , stationAvailable: false}
                    }
                }
                //if (stations[0].status == "Available") {
                //    if ($scope.chargerStatus0 === false) {
                //        alert('Station 0 Is now available');
                //    }
                //    $scope.chargerStatus0 = true;
                //} else {
                //    $scope.chargerStatus0 = false;
                //}
                //if (stations[1].status == "Available") {
                //    if ($scope.chargerStatus1 === false) {
                //        alert('Station 1 Is now available');
                //    }
                //    $scope.chargerStatus1 = true;
                //} else {
                //    $scope.chargerStatus1 = false;
                //}
            });

        };
        loopCheck();
        setInterval(loopCheck, 60000);
    });
