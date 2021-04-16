---
description: El perfil de red describe los objetos que se usan para configurar el sistema para permitir que las máquinas virtuales se comuniquen a través de la red.
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: Servicio de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc85b7a5121a3e7e42f333f829816184b57bd8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686735"
---
# <a name="networking-service"></a>Servicio de red

El perfil de red describe los objetos que se usan para configurar el sistema para permitir que las máquinas virtuales se comuniquen a través de la red. Los objetos de red globales, que se usan para configurar el conmutador de red en el sistema operativo de administración, incluyen las clases [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md), [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)y [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) . Los objetos de red de máquinas virtuales, que se usan para configurar la tarjeta de interfaz de red (NIC) en la máquina virtual, incluyen las clases [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md), [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)y [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) .

La raíz del perfil de red global es la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) . Esta clase representa un dispositivo de conmutador virtual en el sistema operativo de administración. **MSVM \_ VirtualEthernetSwitch** está asociado con instancias de la clase [**MSVM \_ SwitchPort**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) , que representa los puertos del conmutador virtual. Las instancias de las clases **MSVM \_ VirtualEthernetSwitch** y [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) se crean, eliminan y conectan a través de la clase [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) (no se muestra en la ilustración anterior).

El servicio de administración de conmutadores virtuales (VSMS) representa el servicio de red presente en un único host de Hyper-V y contiene métodos para [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que se usan para controlar la definición, la modificación y la destrucción de recursos de red globales como conmutadores virtuales, puertos de conmutadores y puertos Ethernet internos.

La representación del dispositivo NIC Ethernet en la máquina virtual es muy similar a la de cualquier otro dispositivo, como se describe en el [**servicio de administración del sistema virtual**](virtual-system-management-service.md). Las clases [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) y [**MSVM \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md) representan el dispositivo NIC virtual y se configuran mediante una instancia de [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (RASD) asociada. La única característica inusual de esta representación es que, cuando se crea una instancia de la máquina virtual y, a su vez, crea los dispositivos **MSVM \_ EmulatedEthernetPort** y **MSVM \_ SyntheticEthernetPort** , también crea una instancia de [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) asociada para la NIC virtual. Del mismo modo, cuando se guarda o se desactiva la máquina virtual y se destruyen las instancias de **MSVM \_ EmulatedEthernetPort** y **MSVM \_ SyntheticEthernetPort** , también se destruye la instancia de MSVM [**\_ VmLANEndpoint**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) asociada. El propósito de la **\_ LANEndpoint de MSVM** es actuar como un puente para conectar dos puertos de red entre sí. En este caso, se usa para conectar una NIC virtual a un puerto en el dispositivo de conmutador virtual. En otras palabras, conecta las instancias de **MSVM \_ EmulatedEthernetPort** y **MSVM \_ SyntheticEthernetPort** en la máquina virtual a una instancia de MSVM [**\_ EthernetSwitchPort**](msvm-ethernetswitchport.md) determinada en el conmutador virtual. Para conectar un conmutador al exterior, debe enlazar el puerto de Ethernet físico al [**\_ VirtualSwitch de MSVM**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) a través de [**BindExternalEthernetPort**](https://www.bing.com/search?q=**BindExternalEthernetPort**). Adversamente, al conectar un conmutador a la pila de redes del host o a la NIC interna, use ConnectInternal para que una máquina virtual se comunique con el host y no con el mundo externo. [**MSVM \_ ActiveConnection**](msvm-activeconnection.md) conecta un puerto del conmutador con [**el \_ SwitchLANEndpoint de MSVM**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) al que está conectado el puerto en Hyper-V. La existencia de este objeto significa que el puerto del conmutador y **el \_ SwitchLANEndpoint MSVM** están conectados activamente y el puerto Ethernet asociado **con \_ MSVM LANEndpoint** puede comunicarse con la red a través del puerto del conmutador.

 

 



