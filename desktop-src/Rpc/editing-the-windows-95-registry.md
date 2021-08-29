---
title: Edición del registro Windows 95
description: Puede usar REGEDIT para editar el registro Windows 95 para designar un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4442ef9984110fb0d912e4e5e90e00b7d14222bc16044c02f9570fe3e714c066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021664"
---
# <a name="editing-the-windows-95-registry"></a>Edición del registro Windows 95

Puede usar REGEDIT para editar el registro Windows 95 para designar un NSP.

**Para designar un proveedor de servicios de nombre de localizador de Microsoft para Windows 95**

1.  Seleccionar

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Rpc**

2.  Creación de una nueva clave denominada

    **NameService**

3.  Con la **clave NameService** seleccionada, cree los nuevos nombres **StringValue** y modifiquelos para que contengan datos, como se muestra en la tabla siguiente.

    

    | Nombre                     | Datos                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                                |
    | **Protocolo**             | ncacn \_ np<br/>                                                        |
    | **Punto de conexión**             | \\localizador de \\ canalización<br/>                                                  |
    | **NetworkAddress**       | myserver (donde myserver es el nombre del equipo Windows NT)<br/> |
    | **ServerNetworkAddress** | Myserver<br/>                                                         |

    

     

Puede usar REGEDIT para editar el registro Windows 95 para designar un NSP de CDS de DCE.

**Para designar un proveedor de servicios de nombre de CDS de DCE para Windows 95**

1.  Seleccionar

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Rpc**

2.  Creación de una nueva clave denominada

    **NameService**

3.  Con la **clave NameService** seleccionada, cree los nuevos nombres **StringValue** y modifiquelos para que contengan datos, como se muestra en la tabla siguiente.

    

    | Nombre                     | Datos                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                     |
    | **Protocolo**             | ncacn \_ ip \_ tcp<br/>                                        |
    | **Punto de conexión**             | "" (una cadena vacía)<br/>                                  |
    | **NetworkAddress**       | myserver (el nombre del equipo host que ejecuta nsid)<br/> |
    | **ServerNetworkAddress** | myserver (el nombre del equipo host que ejecuta nsid)<br/> |

    

     

    > [!Note]  
    > Debe tener el producto DCE de Digital Equipment Corporation Servicio de directorio de celdas para configurar DCE CDS como proveedor de servicios de nombre. Consulte la documentación proporcionada por Digital Equipment Corporation para obtener información sobre DCE CDS.

     

 

 





