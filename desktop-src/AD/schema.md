---
title: Esquema (AD DS)
description: Active Directory esquema se implementa como un conjunto de instancias de clase de objeto almacenadas en el directorio .
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory esquema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a12d18012abf3e2cf9fc9fdd6831be34d62c88279ad78a0e351534d1899e062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183974"
---
# <a name="schema-ad-ds"></a>Esquema (AD DS)

Active Directory esquema se implementa como un conjunto de instancias de clase de objeto almacenadas en el directorio . Esto es muy diferente de muchos directorios que tienen un esquema pero lo almacenan como un archivo de texto leído en el inicio. Almacenar el esquema en el directorio tiene muchas ventajas. Por ejemplo, las aplicaciones de usuario pueden leerlo para detectar qué objetos y propiedades están disponibles.

Active Directory esquema se puede actualizar dinámicamente. Es decir, una aplicación puede extender el esquema con nuevos atributos y clases y usar las extensiones inmediatamente. Las actualizaciones de esquema se logran mediante la creación o modificación de los objetos de esquema almacenados en el directorio . Al igual que todos los objetos de Active Directory, las listas de control de acceso (ACL) protegen los objetos de esquema, por lo que los usuarios autorizados solo pueden modificar el esquema.

Para obtener más información, [vea Active Directory esquema](active-directory-schema.md).

 

 




