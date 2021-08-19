---
title: Establecer derechos de acceso en todo el objeto
description: Determinados permisos solo se pueden establecer para un objeto completo, como Eliminar y Mostrar contenido. Los permisos específicos de la operación, como el permiso De lectura, también se pueden establecer para todo el objeto para que se apliquen a un objeto completo.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Establecimiento de derechos de acceso en todo el ad de objeto
- objetos de AD, establecer derechos de acceso en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde06726b7333865fe2f4b87b87bec4383a3aeb1799ad6b8772142d5b9fd6eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024783"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Establecer derechos de acceso en todo el objeto

Determinados permisos solo se pueden establecer para un objeto completo, como Eliminar y Mostrar contenido. Los permisos específicos de la operación, como el permiso De lectura, también se pueden establecer para todo el objeto para que se apliquen a un objeto completo.

El siguiente procedimiento se puede usar para establecer permisos para un objeto completo.

**Para establecer permisos para un objeto completo**

1.  Establezca [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ ACETYPE ACCESS \_ \_ ALLOWED** o **ADS \_ ACETYPE ACCESS \_ \_ DENIED**.
2.  Establezca [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **e IADsAccessControlEntry.InheritedObjectType** en **NULL.**

Para obtener más información sobre cómo crear una ACE, vea [Establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE, vea Ejemplo de código para establecer una [ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 