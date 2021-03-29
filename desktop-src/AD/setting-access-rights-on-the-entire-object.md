---
title: Establecer derechos de acceso en todo el objeto
description: Ciertos permisos solo se pueden establecer para un objeto completo, como eliminar y mostrar el contenido. Los permisos específicos de la operación, como el permiso de lectura, también se pueden establecer para el objeto completo, de modo que se apliquen a un objeto completo.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Establecer derechos de acceso en todo el objeto AD
- objetos AD, establecer derechos de acceso en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487394"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Establecer derechos de acceso en todo el objeto

Ciertos permisos solo se pueden establecer para un objeto completo, como eliminar y mostrar el contenido. Los permisos específicos de la operación, como el permiso de lectura, también se pueden establecer para el objeto completo, de modo que se apliquen a un objeto completo.

El siguiente procedimiento se puede usar para establecer permisos para un objeto completo.

**Para establecer permisos para un objeto completo**

1.  Establezca [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ permitido** o **anuncios \_ AceType \_ acceso \_ denegado**.
2.  Establezca [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) y **IADsAccessControlEntry. InheritedObjectType** en **null**.

Para obtener más información sobre cómo crear una ACE, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE, vea el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 