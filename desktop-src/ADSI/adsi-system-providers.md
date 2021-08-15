---
title: Proveedores de servicios ADSI
description: En este tema se proporciona información general sobre los proveedores de servicios ADSI que se proporcionan en el servidor.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, proveedores de servicios
- ADSI de proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66b90aad4e9fa1a6cf6a2229910257f018a411aa7b11b9accca6fcf96dce39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962214"
---
# <a name="adsi-service-providers"></a>Proveedores de servicios ADSI

ADSI incluye los proveedores de servicios enumerados en la tabla siguiente.



| Proveedor de servicios | Descripción                                                                                | Para obtener más información                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implementación del espacio de nombres compatible con el Protocolo ligero de acceso a directorios.<br/> | [Proveedor LDAP ADSI](adsi-ldap-provider.md)<br/>   |
| Winnt<br/> | Implementación del espacio de nombres compatible con Windows.<br/>                               | [Proveedor ADSI WinNT](adsi-winnt-provider.md)<br/> |



 

Otros proveedores de servicios se incluyen como parte de productos distintos de ADSI. A continuación se muestran los proveedores de servicios ADSI implementados por Microsoft.



| Proveedor de servicios | Para obtener más información                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Arquitectura del proveedor ADSI de IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Los métodos y métodos de propiedad expuestos por las interfaces ADSI no son compatibles con todos los proveedores de servicios. Dado que los distintos servicios de directorio varían en los tipos de objetos y propiedades almacenados, usan protocolos y autenticación diferentes, ADSI está diseñado para funcionar sin problemas con proveedores de servicios compatibles. Por lo tanto, hay interfaces, métodos y métodos de propiedad que funcionan con un proveedor de servicios, como LDAP, que pueden no funcionar en otro, como WinNT.

Esta sección contiene información específica del proveedor, como el formato ADsPath, una lista de objetos ADSI usados para ese proveedor de servicios y la información de tipo de datos y sintaxis para los proveedores de servicios incluidos con ADSI. También hay una descripción resumida de las interfaces ADSI compatibles con cada proveedor incluido con ADSI.

En ADSI, los distintos proveedores están asociados a archivos DLL diferentes. El proveedor LDAP está asociado a Adsldp.dll, Adsldpc.dll y Adsmsext.dll. El proveedor WinNT está asociado a Adsnt.dll. El proveedor de ENRUTADOR está asociado a Activeds.dll.

> [!Note]  
> No suponga que los proveedores adsi predeterminados son seguros para subprocesos. Los desarrolladores de aplicaciones multiproceso deben coordinar el acceso entre subprocesos mediante el uso adecuado de objetos de sincronización, como semáforos, exclusiones mutuas, secciones críticas, entre otros.

 

Para obtener más información sobre los proveedores de servicios [ADSI, vea Enrutador ADSI](adsi-router.md) y Compatibilidad con proveedores [de interfaces ADSI](provider-support-of-adsi-interfaces.md).

 

