---
title: Integración de extensiones de esquema con la interfaz de usuario
description: Las herramientas de administración de Active Directory Domain Services utilizan una arquitectura común para conectar la interfaz de usuario administrativa con el esquema de directorio.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656225"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integración de extensiones de esquema con la interfaz de usuario

Las herramientas de administración de Active Directory Domain Services utilizan una arquitectura común para conectar la interfaz de usuario administrativa con el esquema de directorio. El eje de esta arquitectura es la clase de objeto **displaySpecifier** . Los especificadores de presentación y su uso se describen en detalle en [extensión de la interfaz de usuario para objetos de directorio](extending-the-user-interface-for-directory-objects.md).

Al crear una nueva clase mediante la creación de subclases de una clase existente, puede aprovechar la interfaz de usuario existente para la superclase mediante la copia del especificador de presentación de la superclase. Una manera sencilla de copiar el especificador de presentación de una clase es exportarlo a un archivo LDIF mediante LDIFDE, editar el nombre distintivo y el CN, y luego importar el archivo LDIF modificado. Si la subclase tiene atributos adicionales, tendrá que proporcionar páginas de propiedades adicionales para admitir la edición. Si la subclase tiene propiedades adicionales que deben tener, debe proporcionar las páginas de extensión del cuadro de diálogo de creación, ya que la interfaz de usuario proporcionada por la superclase no tiene forma de crear estos nuevos atributos.

 

 




