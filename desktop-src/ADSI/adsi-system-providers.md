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
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656394"
---
# <a name="adsi-service-providers"></a>Proveedores de servicios ADSI

ADSI incluye los proveedores de servicios que se enumeran en la tabla siguiente.



| Proveedor de servicios | Descripción                                                                                | Para obtener más información                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implementación de espacio de nombres compatible con el Protocolo ligero de acceso a directorios.<br/> | [Proveedor LDAP de ADSI](adsi-ldap-provider.md)<br/>   |
| WinNT<br/> | Implementación de espacio de nombres compatible con Windows.<br/>                               | [Proveedor WinNT de ADSI](adsi-winnt-provider.md)<br/> |



 

Otros proveedores de servicios se incluyen como parte de productos distintos de ADSI. A continuación se indican los proveedores de servicios ADSI implementados por Microsoft.



| Proveedor de servicios | Para obtener más información                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Arquitectura del proveedor ADSI de IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Todos los proveedores de servicios no admiten los métodos y métodos de propiedad expuestos por las interfaces ADSI. Dado que los distintos servicios de directorio varían en los tipos de objetos y propiedades almacenados, usan protocolos y autenticación diferentes, ADSI está diseñado para funcionar sin problemas con proveedores de servicios compatibles. Por lo tanto, hay interfaces, métodos y métodos de propiedad que funcionan con un proveedor de servicios, como LDAP, que puede que no funcionen en otro, como Winnt.

Esta sección contiene información específica del proveedor, como el formato de ADsPath, una lista de objetos ADSI utilizados para ese proveedor de servicios e información sobre el tipo de datos y la sintaxis de los proveedores de servicios incluidos con ADSI. También hay una descripción breve de las interfaces ADSI que admite cada proveedor incluido con ADSI.

En ADSI, los distintos proveedores están asociados a distintos archivos dll. El proveedor LDAP está asociado a Adsldp.dll, Adsldpc.dll y Adsmsext.dll. El proveedor de WinNT está asociado a Adsnt.dll. El proveedor del enrutador está asociado a Activeds.dll.

> [!Note]  
> No asuma que los proveedores ADSI predeterminados son seguros para subprocesos. Los desarrolladores de aplicaciones multiproceso deben coordinar el acceso entre subprocesos mediante el uso correcto de objetos de sincronización como semáforos, exclusiones mutuas, secciones críticas, etc.

 

Para obtener más información acerca de los proveedores de servicios ADSI, consulte compatibilidad con el [enrutador ADSI](adsi-router.md) y el [proveedor de interfaces ADSI](provider-support-of-adsi-interfaces.md).

 

