---
title: Integración de extensiones de esquema con el Interfaz de usuario
description: Las herramientas de administración de Active Directory Domain Services usan una arquitectura común para conectar la interfaz de usuario administrativa al esquema de directorio.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d951ec51d7453ee92cf90ddcb28ddb8219d3056b1edb96d16bf15494fe956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187214"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integración de extensiones de esquema con el Interfaz de usuario

Las herramientas de administración de Active Directory Domain Services usan una arquitectura común para conectar la interfaz de usuario administrativa al esquema de directorio. La pieza central de esta arquitectura es la **clase de objeto displaySpecifier.** Los especificadores de visualización y su uso se describen en detalle en [Extending the Interfaz de usuario for Directory Objects](extending-the-user-interface-for-directory-objects.md).

Al crear una nueva clase mediante la creación de subclases de una clase existente, puede aprovechar la interfaz de usuario existente para la superclase copiando el especificador de presentación de la superclase. Una manera fácil de copiar el especificador de visualización de una clase es exportarlo a un archivo LDIF mediante LDIFDE, editar el nombre distintivo y cn y, a continuación, importar el archivo LDIF modificado. Si la subclase tiene atributos adicionales, deberá proporcionar páginas de propiedades adicionales para admitir la edición. Si la subclase tiene propiedades must-have adicionales, deberá proporcionar páginas de extensión de cuadro de diálogo de creación, ya que la interfaz de usuario proporcionada por la superclase no tiene ninguna manera de crear estos nuevos atributos.

 

 




