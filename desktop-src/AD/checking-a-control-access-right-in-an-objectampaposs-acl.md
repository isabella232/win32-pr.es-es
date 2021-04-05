---
title: Comprobar un derecho de acceso a control en la ACL de un objeto
description: Para comprobar un derecho de acceso de control en la ACL de un objeto, utilice la función AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Comprobando el derecho de acceso de un control en un anuncio de ACL de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077559"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>Comprobar un derecho de acceso a control en la ACL de un objeto

Para comprobar un derecho de acceso de control en la ACL de un objeto, utilice la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) . Para usar esta función, una aplicación requiere un puntero al [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para el objeto en lugar de una interfaz [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) a un objeto com del descriptor de seguridad de ADSI.

Use los pasos siguientes para comprobar el acceso de un derecho de acceso controlado en un objeto:

1.  Obtiene un puntero de la interfaz [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) al objeto.
2.  Use el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para obtener el descriptor de seguridad del objeto. El nombre de la propiedad que contiene el descriptor de seguridad es [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor). La propiedad se devuelve como un puntero a una estructura de [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .
3.  Use la estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para comprobar los permisos para el derecho de acceso de control especificado para el cliente especificado.

En el código de ejemplo del [código de ejemplo para comprobar el derecho de acceso a un control en la ACL de un objeto](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) se muestra, en detalle, cómo hacerlo.

 

 