---
description: Las siguientes funciones se usan con DDE de red.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funciones DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697866"
---
# <a name="network-dde-functions"></a>Funciones DDE de red

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Las siguientes funciones se usan con DDE de red.



| Función                                                   | Descripción                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Recupera el descriptor de seguridad asociado al recurso compartido DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Recupera las opciones asociadas a un recurso compartido DDE que se encuentra en la lista de recursos compartidos de confianza del usuario del servidor.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Determina si una aplicación y una cadena de tema ("*appname* \| *TopicName*") utiliza la sintaxis correcta.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Determina si un nombre de recurso compartido utiliza la sintaxis correcta.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Establece el descriptor de seguridad asociado al recurso compartido DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Concede el estado de confianza del recurso compartido DDE especificado en el contexto del usuario actual.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Crea y agrega un nuevo recurso compartido DDE al administrador de bases de datos de recursos compartidos DDE (DSDM).                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Elimina un recurso compartido DDE del DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Recupera la lista de recursos compartidos DDE disponibles.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Recupera la información del recurso compartido DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Establece la información de recursos compartidos DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Recupera los nombres de todos los recursos compartidos DDE de red que son de confianza en el contexto del proceso de llamada.                 |



 

 

 



