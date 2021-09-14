---
description: ICE90 envía una advertencia si encuentra que el directorio de un acceso directo se ha especificado como una propiedad pública.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074511"
---
# <a name="ice90"></a>ICE90

ICE90 envía una advertencia si encuentra que el directorio de un acceso directo se ha especificado como una propiedad pública. Los nombres de [las propiedades públicas](public-properties.md) se escriben en mayúsculas. Es posible que un acceso directo especificado por una propiedad pública no funcione si cambia el valor de [**la propiedad ALLUSERS.**](allusers.md)

Esta acción personalizada de ICE valida la tabla de accesos directos y usa la tabla Directory. Si la tabla Directory no está presente, devuelve sin validar la tabla de accesos directos y no muestra errores ni advertencias.

## <a name="result"></a>Resultado

ICE90 publica la advertencia siguiente.



| Error ICE90                                                                                                                                                                                                                    | Descripción                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| El acceso directo \[ "1" tiene un directorio que es una propiedad \] pública (ALL CAPS) y está en el directorio de perfil de usuario. Esto produce un problema si el valor de la [**propiedad ALLUSERS**](allusers.md) cambia en la secuencia de la interfaz de usuario. | El directorio de un acceso directo se ha especificado como una propiedad pública. |



 

## <a name="example"></a>Ejemplo

ICE90 notifica la advertencia siguiente para el ejemplo:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

En este ejemplo, MYDIR se encuentra en un perfil de usuario. ICE90 envía una advertencia porque la ubicación del directorio de destino se especifica mediante una propiedad pública, MYDIR. Un usuario puede cambiar la propiedad MYDIR [**o ALLUSERS.**](allusers.md) Si **ALLUSERS** se establece para [](installation-context.md)el contexto de instalación por equipo y MYDIR está en un perfil de usuario, el archivo de acceso directo de MYDIR se copia en el perfil "Todos los usuarios" y no en el perfil de un usuario determinado. Si **ALLUSERS se** establece para el contexto de instalación por usuario, el archivo de acceso directo de MYDIR se copia en el perfil de un usuario determinado y no está disponible para otros usuarios.

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Directorio\_ |
|-----------|-------------|
| Acceso directo1 | MYDIR       |



 

[Tabla de directorios](directory-table.md) (parcial)



| Directorio | Elemento primario \_ del directorio |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



