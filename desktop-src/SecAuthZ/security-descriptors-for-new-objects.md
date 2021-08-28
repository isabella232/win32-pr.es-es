---
description: Al crear un objeto protegible, puede asignar un descriptor de seguridad al nuevo objeto.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descriptores de seguridad para nuevos objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38edc927f1f017e3f102194b0a4aac5d0442ec730e8480a00c054add0935a62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907345"
---
# <a name="security-descriptors-for-new-objects"></a>Descriptores de seguridad para nuevos objetos

Al crear un objeto protegible, puede asignar un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) al nuevo objeto. Las funciones para crear objetos protegibles, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), tienen un parámetro que apunta a la estructura [**ATRIBUTOS \_**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) DE SEGURIDAD que puede contener un puntero al descriptor de seguridad del nuevo objeto. Para obtener código de ejemplo que compila un descriptor de seguridad y, a continuación, llama a **RegCreateKeyEx** para asignar el descriptor de seguridad a una nueva clave del Registro, vea Crear un descriptor de seguridad para un nuevo objeto en [C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md)

El componente o servidor del sistema que administra el objeto puede almacenar el descriptor de seguridad especificado o predeterminado para que sea un atributo persistente del objeto. Si el creador de un objeto no especifica un descriptor de seguridad, el sistema usa información de seguridad heredada o predeterminada para crear un descriptor de seguridad. Puede usar funciones para cambiar la información en el descriptor de seguridad de un objeto.

Los objetos de servicio de directorio, archivos, directorios, claves del Registro y escritorios son objetos protegibles que pueden tener un objeto primario. Al crear uno de estos objetos, el sistema comprueba si hay ACE heredables en el descriptor de seguridad del objeto primario. Normalmente, el sistema combina todas las ACE heredables en las ACL del descriptor de seguridad del nuevo objeto. Puede evitar que una DACL o SACL herede las ACE estableciendo los bits de control SE DACL PROTECTED o SE SACL PROTECTED en los bits de control del descriptor de \_ \_ \_ \_ seguridad. Para obtener más información, vea [Herencia ace.](ace-inheritance.md)

 

 
