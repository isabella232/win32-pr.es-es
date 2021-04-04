---
description: ICE90 publica una advertencia si detecta que se ha especificado el directorio de un acceso directo como una propiedad pública.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908842"
---
# <a name="ice90"></a>ICE90

ICE90 publica una advertencia si detecta que se ha especificado el directorio de un acceso directo como una propiedad pública. Los nombres de [las propiedades públicas](public-properties.md) se escriben en mayúsculas. Un acceso directo especificado por una propiedad pública puede no funcionar si cambia el valor de la propiedad [**AllUsers**](allusers.md) .

Esta acción personalizada de ICE valida la tabla de acceso directo y usa la tabla de directorio. Si la tabla del directorio no está presente, devuelve sin validar la tabla de accesos directos y no envía ningún error ni ADVERTENCIA.

## <a name="result"></a>Resultado

ICE90 envía la siguiente advertencia.



| Error ICE90                                                                                                                                                                                                                    | Descripción                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| El acceso directo ' \[ 1 \] ' tiene un directorio que es una propiedad pública (todos los extremos) y está en el directorio del perfil de usuario. Esto produce un problema si el valor de la propiedad [**AllUsers**](allusers.md) cambia en la secuencia de la interfaz de usuario. | El directorio de un acceso directo se ha especificado como una propiedad pública. |



 

## <a name="example"></a>Ejemplo

ICE90 notifica la siguiente advertencia para el ejemplo:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

En este ejemplo, MYDIR está en un perfil de usuario. ICE90 publica una advertencia porque la ubicación del directorio de destino se especifica mediante una propiedad pública, MYDIR. Un usuario puede cambiar MYDIR o la propiedad [**AllUsers**](allusers.md) . Si se establece **AllUsers** para el [contexto de instalación](installation-context.md)por equipo y MYDIR está en un perfil de usuario, el archivo de acceso directo de MYDIR se copia en el perfil "todos los usuarios" y no en el perfil de un usuario determinado. Si se establece **AllUsers** para el contexto de instalación por usuario, el archivo de acceso directo de MYDIR se copia en el perfil de un usuario determinado y no está disponible para otros usuarios.

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Directorio\_ |
|-----------|-------------|
| Shortcut1 | MYDIR       |



 

[Tabla de directorio](directory-table.md) (parcial)



| Directorio | Directorio \_ primario |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



