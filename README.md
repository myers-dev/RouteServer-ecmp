Code="MaximumLocalNetworkSitesLimitReachedForGateway" Message="Maximum connection limit reached. Current site to site connections : 31, max limit : 30" Details=[]


../supplementals/active_routes.sh spoke-vnet-vm-vmLinux-0 $RG
Source                 State    Address Prefix    Next Hop Type          Next Hop IP
---------------------  -------  ----------------  ---------------------  -------------
Default                Active   10.0.0.0/16       VnetLocal
Default                Active   10.1.0.0/16       VNetPeering
VirtualNetworkGateway  Active   10.2.0.0/16       VirtualNetworkGateway  10.1.1.17
VirtualNetworkGateway  Active   10.2.0.0/16       VirtualNetworkGateway  10.1.1.12
VirtualNetworkGateway  Active   10.2.0.0/16       VirtualNetworkGateway  10.1.1.13
VirtualNetworkGateway  Active   10.2.0.0/16       VirtualNetworkGateway  10.1.1.9
VirtualNetworkGateway  Active   0.0.0.0/0         VirtualNetworkGateway  10.1.1.17
VirtualNetworkGateway  Active   0.0.0.0/0         VirtualNetworkGateway  10.1.1.12
VirtualNetworkGateway  Active   0.0.0.0/0         VirtualNetworkGateway  10.1.1.13
VirtualNetworkGateway  Active   0.0.0.0/0         VirtualNetworkGateway  10.1.1.9

az network routeserver peering list --routeserver RouteServer --resource-group RS -o table
Name    PeerAsn    PeerIp     ProvisioningState    ResourceGroup
------  ---------  ---------  -------------------  ---------------
CSR0    65555      10.1.1.17  Succeeded            RS
CSR1    65555      10.1.1.12  Succeeded            RS
CSR2    65555      10.1.1.13  Succeeded            RS
CSR3    65555      10.1.1.9   Succeeded            RS
CSR4    65555      10.1.1.4   Failed               RS
CSR5    65555      10.1.1.19  Failed               RS
CSR6    65555      10.1.1.18  Failed               RS
CSR7    65555      10.1.1.16  Failed               RS
CSR8    65555      10.1.1.11  Failed               RS
CSR9    65555      10.1.1.10  Failed               RS
CSR10   65555      10.1.1.7   Failed               RS
CSR11   65555      10.1.1.20  Failed               RS
CSR12   65555      10.1.1.8   Failed               RS
CSR13   65555      10.1.1.15  Failed               RS
CSR14   65555      10.1.1.14  Failed               RS
CSR15   65555      10.1.1.6   Failed               RS


./supplementals/active_routes.sh remote-vnet-vm-vmLinux-0 $RG
Source                 State    Address Prefix     Next Hop Type          Next Hop IP
---------------------  -------  -----------------  ---------------------  -------------
Default                Active   10.2.0.0/16        VnetLocal
VirtualNetworkGateway  Active   192.168.100.5/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.5/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.10/32  VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.10/32  VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.15/32  VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.15/32  VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.4/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.4/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.2/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.2/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.14/32  VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.14/32  VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.1/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.1/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.12/32  VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.12/32  VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   0.0.0.0/0          VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.13/32  VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.13/32  VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.8/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.8/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.7/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.7/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.11/32  VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.11/32  VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.6/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.6/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   10.0.0.0/16        VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   10.0.0.0/16        VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.9/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.9/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.0/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.0/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   192.168.100.3/32   VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   192.168.100.3/32   VirtualNetworkGateway  10.2.0.5
VirtualNetworkGateway  Active   10.1.0.0/16        VirtualNetworkGateway  10.2.0.4
VirtualNetworkGateway  Active   10.1.0.0/16        VirtualNetworkGateway  10.2.0.5



IDX=0
for peer in ${peers}; do
    az network route-table route create --address-prefix 0.0.0.0/0 \
                                    --name default${IDX} \
                                    --next-hop-type VirtualAppliance \
                                    --route-table-name RT \
                                    --resource-group ${RG} \
                                    --next-hop-ip-address $peer
    let IDX=$IDX+1
    echo $IDX
done

(RouteConflict) Route: default1 conflicts with Route: default0. Routes cannot have the same AddressPrefix.