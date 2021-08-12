---
title: Registro del proveedor de servicios
description: Registro del proveedor de servicios
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Administrador de dispositivos,registering service providers
- Administrador de dispositivos, registrar proveedores de servicios
- guía de programación, registro de proveedores de servicios
- proveedores de servicios, registrar proveedores de servicios
- crear proveedores de servicios, registrar proveedores de servicios
- registrar proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f480fff04d34cf671bdc37e3bcded92c73f20d31d2fb67e4d6e41593a724d392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584305"
---
# <a name="registering-the-service-provider"></a>Registro del proveedor de servicios

Además de registrarse como un objeto COM, un proveedor de servicios debe registrarse como complemento para Windows Media Administrador de dispositivos. Para registrarse, un proveedor de servicios debe crear la siguiente clave del Registro:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

En esta clave, < *nombre del* proveedor de > es el nombre del archivo DLL; Por ejemplo, el proveedor de servicios de ejemplo usa MsHDSP. La clave ProgID debe tener un valor de cadena que corresponda al CLSID del proveedor de servicios. Por ejemplo, el proveedor de servicios de ejemplo tiene el valor "MDServiceProviderHD.MDServiceProviderHD".

La implementación del proveedor de servicios de ejemplo de DLLRegisterServer en Mdsp.cpp agrega esta clave del Registro al registrar el archivo DLL del proveedor de servicios de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




