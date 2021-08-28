---
description: Las siguientes funciones se implementan mediante un archivo DLL de proveedor de red para comunicarse con el enrutador de varios proveedores (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funciones implementadas por proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892bcb5c19f54e5de667eb72119f6b9e5fc9b183b8d5038ce37b7e556ae5d3a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016325"
---
# <a name="functions-implemented-by-network-providers"></a>Funciones implementadas por proveedores de red

Las siguientes funciones se implementan mediante un archivo DLL de proveedor de red para comunicarse con [*el enrutador de varios*](/windows/desktop/SecGloss/m-gly) proveedores (MPR). Tenga en cuenta que [un proveedor de red](capabilities-functions.md) solo debe implementar las funciones de funcionalidades. La implementación de los otros tipos de funciones es opcional y depende de los requisitos del proveedor de red.



| Conjunto de funciones                                                                                    | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funciones de funcionalidades](capabilities-functions.md)<br/>                                 | Permite al autor de la llamada determinar las funcionalidades del proveedor de red.<br/>                                                                |
| [Funciones de nombre de usuario](user-name-functions.md)<br/>                                       | Solicita al proveedor de red el nombre de usuario asociado a una conexión.<br/>                                                            |
| [Funciones de redirección de dispositivos](device-redirecting-functions.md)<br/>                     | Permite a un proveedor de red redirigir dispositivos, letras de unidad y puertos LPT que son estándar en el sistema operativo Microsoft MS-DOS.<br/> |
| [Funciones de cuadro de diálogo específicas del proveedor](provider-specific-dialog-box-functions.md)<br/> | Permite que un proveedor de red muestre o actúe sobre información específica de la red.<br/>                                                            |
| [Funciones administrativas](administrative-functions.md)<br/>                             | Permite que un proveedor de red muestre o actúe en directorios de red especiales.<br/>                                                             |
| [Funciones de enumeración](enumeration-functions.md)<br/>                                   | Permite al usuario examinar los recursos de red.<br/>                                                                                            |



 

Para obtener más información sobre cómo crear y registrar un proveedor de red, vea [Implementar](implementing-a-network-provider.md) un proveedor de red y Registrar proveedores de red [y administradores de credenciales.](registering-network-providers-and-credential-managers.md)

 

