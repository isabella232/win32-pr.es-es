---
title: Esquema (AD DS)
description: Active Directory esquema se implementa como un conjunto de instancias de clase de objeto almacenadas en el directorio.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory de esquema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "103785422"
---
# <a name="schema-ad-ds"></a>Esquema (AD DS)

Active Directory esquema se implementa como un conjunto de instancias de clase de objeto almacenadas en el directorio. Esto es muy diferente que muchos directorios que tienen un esquema, pero lo almacenan como un archivo de texto leído en el inicio. Almacenar el esquema en el directorio tiene muchas ventajas. Por ejemplo, las aplicaciones de usuario pueden leerla para detectar qué objetos y propiedades están disponibles.

Active Directory esquema se puede actualizar dinámicamente. Es decir, una aplicación puede extender el esquema con nuevos atributos y clases y usar las extensiones inmediatamente. Las actualizaciones de esquema se realizan mediante la creación o modificación de los objetos de esquema almacenados en el directorio. Al igual que todos los objetos de Active Directory, las listas de control de acceso (ACL) protegen los objetos de esquema, por lo que solo los usuarios autorizados pueden modificar el esquema.

Para obtener más información, vea [esquema de Active Directory](active-directory-schema.md).

 

 




