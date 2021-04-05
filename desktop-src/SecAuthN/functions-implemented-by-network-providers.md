---
description: Las siguientes funciones las implementa una DLL de proveedor de red para comunicarse con el enrutador de proveedor múltiple (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funciones implementadas por los proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002762"
---
# <a name="functions-implemented-by-network-providers"></a>Funciones implementadas por los proveedores de red

Las siguientes funciones las implementa una DLL de proveedor de red para comunicarse con el [*enrutador de proveedor múltiple*](/windows/desktop/SecGloss/m-gly) (MPR). Tenga en cuenta que solo las [funciones de funcionalidad](capabilities-functions.md) deben ser implementadas por un proveedor de red. La implementación de los demás tipos de funciones es opcional y depende de los requisitos del proveedor de red.



| Conjunto de funciones                                                                                    | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funciones de funcionalidad](capabilities-functions.md)<br/>                                 | Permite al llamador determinar las capacidades del proveedor de red.<br/>                                                                |
| [Funciones de nombre de usuario](user-name-functions.md)<br/>                                       | Solicita al proveedor de red el nombre de usuario asociado a una conexión.<br/>                                                            |
| [Funciones de redireccionamiento de dispositivos](device-redirecting-functions.md)<br/>                     | Permite a un proveedor de red redirigir dispositivos, Letras de unidad y puertos LPT que son estándar en el sistema operativo Microsoft MS-DOS.<br/> |
| [Funciones del cuadro de diálogo específicas del proveedor](provider-specific-dialog-box-functions.md)<br/> | Permite a un proveedor de red mostrar o actuar en la información específica de la red.<br/>                                                            |
| [Funciones administrativas](administrative-functions.md)<br/>                             | Permite que un proveedor de red muestre o actúe en directorios de red especiales.<br/>                                                             |
| [Funciones de enumeración](enumeration-functions.md)<br/>                                   | Permite al usuario examinar los recursos de red.<br/>                                                                                            |



 

Para obtener más información acerca de cómo crear y registrar un proveedor de red, consulte [implementación de un proveedor de red](implementing-a-network-provider.md) y [registro de proveedores de redes y administradores de credenciales](registering-network-providers-and-credential-managers.md).

 

