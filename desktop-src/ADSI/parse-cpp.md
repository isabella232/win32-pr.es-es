---
title: Analiza. CPP
description: En el componente de proveedor de ejemplo, un ejemplo de código del analizador de rutas de acceso del servicio de directorio está en Parse. cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- Análisis ADSI de Parse. cpp
- Analizador de rutas ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ee4df5c1c709fde724385fdf5d5cddbafef338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993847"
---
# <a name="parsecpp"></a>Analiza. CPP

En el componente de proveedor de ejemplo, un ejemplo de código del analizador de rutas de acceso del servicio de directorio está en Parse. cpp. El analizador de rutas de acceso es un componente clave de los componentes del proveedor de ADs. Comprueba la validez sintáctica de una ruta de acceso de anuncios que se pasa a este proveedor. Si la sintaxis es válida, se construye una estructura **OBJECTINFO** , que contiene una versión en componentes de ADspath para este objeto.

Tenga en cuenta que esto es solo una comprobación de sintaxis. En lugar de tener en común cada nueva iteración de path, toda la comprobación de la ruta de acceso debe cumplir las reglas de gramática establecidas por el analizador.

En la tabla siguiente se enumeran las funciones y los métodos implementados en Parse. cpp.



| Elemento                      | Descripción                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analiza el ADspath que se le ha pasado. Esta función sigue las siguientes reglas de gramática: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analiza las siguientes reglas de gramática: <SampleDSObject> -> " \\ " " \\ <identifier> " \\<Pathname><br/>                                            |
| **ProviderName**          | Agrega en el nombre de proveedor sintácticamente correcto si no existe.                                                                                                          |
| **PathName**              | Analiza las siguientes reglas de gramática: <Pathname>  ->  <Component> " \\ \\ " <Pathname> o<br/> <Pathname> -> <Component><br/> |
| **Componente**             | Analiza las siguientes reglas de gramática: <Identifier> o<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Constructor estándar.                                                                                                                                                  |
| **CLexer:: ~ CLexer**       | Destructor estándar.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera el siguiente carácter único.                                                                                                                                       |
| **CLexer::P ushBackToken** | Realiza una copia de seguridad hasta el inicio del último token.                                                                                                                               |
| **CLexer::P ushbackChar**  | Realiza una copia de seguridad de un carácter.                                                                                                                                                |
| **CLexer::IsKeyword**     | Comprueba la lista de palabras clave. Definido en Globals. h).                                                                                                                          |
| **AddComponent**          | Agrega este componente a la matriz de componentes.                                                                                                                            |
| **AddProviderName**       | Agrega un nombre de proveedor sintácticamente correcto a la estructura **OBJECTINFO** .                                                                                            |
| **AddRootRDN**            | Agrega el nombre del nombre distintivo relativo (RDN) raíz sintácticamente correcto a la estructura **OBJECTINFO** .                                                            |
| **SetType**               | Establece el tipo del objeto.                                                                                                                                           |
| **Tipo**                  | Analiza el tipo > "usuario" "grupo", etc \| .                                                                                                                          |



 

 

 





