---
description: El perfil de red describe los objetos usados para configurar el sistema para permitir que las máquinas virtuales se comuniquen a través de la red.
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: Servicio de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5482948a2fc4990b865ac99838e75ccb502d0684e5d81dcb5b44ee7ca5145f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993604"
---
# <a name="networking-service"></a>Servicio de red

El perfil de red describe los objetos usados para configurar el sistema para permitir que las máquinas virtuales se comuniquen a través de la red. Los objetos de red globales, que se usan para configurar el conmutador de red en el sistema operativo de administración, incluyen las clases [**Msvm \_ VirtualEthernetSwitchManagementService,**](msvm-virtualethernetswitchmanagementservice.md) [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)y [**Msvm \_ EthernetSwitchPort.**](msvm-ethernetswitchport.md) Los objetos de red de máquina virtual, que se usan para configurar la tarjeta de interfaz de red (NIC) en la máquina virtual, incluyen las clases [**Msvm \_ EmulatedEthernetPort,**](msvm-emulatedethernetport.md) [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)y [**Msvm \_ LANEndpoint.**](msvm-lanendpoint.md)

La raíz del perfil de red global es la [**\_ clase VirtualEthernetSwitch de Msvm.**](msvm-virtualethernetswitch.md) Esta clase representa un dispositivo de conmutador virtual en el sistema operativo de administración. **Msvm \_ VirtualEthernetSwitch está** asociado a instancias de la clase [**\_ SwitchPort de Msvm,**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) que representa los puertos del conmutador virtual. Las instancias de las clases **\_ Msvm VirtualEthernetSwitch** y [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) se crean, eliminan y conectan a través de la clase [**\_ Msvm VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) (no se muestra en la ilustración anterior).

Virtual Switch Management Service (VSMS) representa el servicio de red presente en un único host de Hyper-V y contiene métodos para [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que se usa para controlar la definición, modificación y destrucción de recursos de red globales, como conmutadores virtuales, puertos switch y puertos Ethernet internos.

La representación del dispositivo NIC Ethernet en la máquina virtual es muy similar a la de cualquier otro dispositivo, como se describe en el servicio [**de administración de sistemas virtuales**](virtual-system-management-service.md). Las clases [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) y [**Msvm \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md) representan el dispositivo NIC virtual y se configuran a través de una instancia de [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (RASD) asociada. La única característica inusual de esta representación es que, cuando se crea una instancia de la máquina virtual y, a su vez, crea los **dispositivos Msvm \_ EmulatedEthernetPort** y **Msvm \_ SyntheticEthernetPort,** también crea una instancia de [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) asociada para la NIC virtual. Del mismo modo, cuando la máquina virtual se guarda o se apaga y se destruyen las instancias **Msvm \_ EmulatedEthernetPort** y **Msvm \_ SyntheticEthernetPort,** también se destruye la instancia de [**\_ VmLANEndpoint de Msvm**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) asociada. El propósito de **Msvm \_ LANEndpoint** es servir como puente para conectar dos puertos de red entre sí. En este caso, se usa para conectar una NIC virtual a un puerto en el dispositivo de conmutador virtual. En otras palabras, conecta las instancias **Msvm \_ EmulatedEthernetPort** y **Msvm \_ SyntheticEthernetPort** de la máquina virtual a una instancia determinada de [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) en el conmutador virtual. Para conectar un conmutador al exterior, debe enlazar el puerto Ethernet físico al conmutador virtual [**de Msvm \_**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) a través de [**BindExternalEthernetPort**](https://www.bing.com/search?q=**BindExternalEthernetPort**). Adverso, al conectar un conmutador a la pila de red del host o a la NIC interna, use ConnectInternal para que una máquina virtual hable con el host y no con el mundo exterior. [**Msvm \_ ActiveConnection**](msvm-activeconnection.md) conecta un puerto de conmutador al punto de [**\_ conexión SwitchLANEndpoint de Msvm**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) al que está conectado el puerto dentro de Hyper-V. La existencia de este objeto significa que el puerto del conmutador y el punto de conexión **\_ SwitchLANEndpoint de Msvm** están conectados activamente y el puerto Ethernet asociado a **Msvm \_ LANEndpoint** puede comunicarse con la red a través del puerto del conmutador.

 

 



