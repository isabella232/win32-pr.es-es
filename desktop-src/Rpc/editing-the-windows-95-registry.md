---
title: Editar el registro de Windows 95
description: Puede usar regedit para modificar el registro de Windows 95 para designar un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903788"
---
# <a name="editing-the-windows-95-registry"></a>Editar el registro de Windows 95

Puede usar regedit para modificar el registro de Windows 95 para designar un NSP.

**Para designar un proveedor de servicios de nombres de Microsoft Locator para Windows 95**

1.  Seleccionar

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **RPC**

2.  Cree una nueva clave denominada

    **NameService**

3.  Con la clave **NameService** seleccionada, cree los nuevos nombres de **valorstring** y modifíquelo para que contengan los datos, tal como se muestra en la tabla siguiente.

    

    | Nombre                     | Datos                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                                |
    | **Protocolo**             | NP de ncacn \_<br/>                                                        |
    | **Punto de conexión**             | \\Localizador de canalización \\<br/>                                                  |
    | **NetworkAddress**       | mi Server (donde he Server es el nombre del equipo Windows NT)<br/> |
    | **ServerNetworkAddress** | myserver<br/>                                                         |

    

     

Puede usar regedit para modificar el registro de Windows 95 para designar un CD de DCE.

**Para designar un proveedor de servicios de nombres de CDS de DCE para Windows 95**

1.  Seleccionar

    **HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **RPC**

2.  Cree una nueva clave denominada

    **NameService**

3.  Con la clave **NameService** seleccionada, cree los nuevos nombres de **valorstring** y modifíquelo para que contengan los datos, tal como se muestra en la tabla siguiente.

    

    | Nombre                     | Datos                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                     |
    | **Protocolo**             | \_TCP IP \_ ncacn<br/>                                        |
    | **Punto de conexión**             | "" (una cadena vacía)<br/>                                  |
    | **NetworkAddress**       | mi Server (el nombre del equipo host que ejecuta NSID)<br/> |
    | **ServerNetworkAddress** | mi Server (el nombre del equipo host que ejecuta NSID)<br/> |

    

     

    > [!Note]  
    > Para configurar los CD de DCE como proveedor de servicios de nombres, debe disponer del producto DCE de Digital Equipment Corporation Servicio de directorio de celdas. Consulte la documentación proporcionada por Digital Equipment Corporation para obtener información acerca de los CD de DCE.

     

 

 





