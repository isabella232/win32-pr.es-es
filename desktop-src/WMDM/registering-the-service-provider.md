---
title: Registrar el proveedor de servicios
description: Registrar el proveedor de servicios
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Administrador de dispositivos, registrar proveedores de servicios
- Administrador de dispositivos, registrar proveedores de servicios
- Guía de programación, registrar proveedores de servicios
- proveedores de servicios, registrar proveedores de servicios
- creación de proveedores de servicios, registro de proveedores de servicios
- registrando proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075260"
---
# <a name="registering-the-service-provider"></a>Registrar el proveedor de servicios

Además de registrarse como un objeto COM, se debe registrar un proveedor de servicios como un complemento de Windows Media Administrador de dispositivos. Para registrarse, un proveedor de servicios debe crear la siguiente clave del registro:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

En esta clave, < *el nombre del proveedor de servicios* > es el nombre del archivo dll; por ejemplo, el proveedor de servicios de ejemplo usa MsHDSP. La clave ProgID debe tener un valor de cadena que se corresponda con el CLSID de su proveedor de servicios. Por ejemplo, el proveedor de servicios de ejemplo tiene el valor "MDServiceProviderHD. MDServiceProviderHD".

La implementación del proveedor de servicios de ejemplo de DLLRegisterServer en Mdsp. cpp agrega esta clave del registro al registrar la DLL del proveedor de servicios de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




