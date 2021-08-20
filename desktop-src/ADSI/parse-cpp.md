---
title: Analizar. Cpp
description: En el componente de proveedor de ejemplo, un ejemplo de código del analizador de rutas de acceso del servicio de directorio está en Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- parse.cpp ADSI
- ADSI del analizador de rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544ab295318ac80ed19df39a7e5837b566615903a8d8bb963b6fdd5435efde8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023293"
---
# <a name="parsecpp"></a>Analizar. Cpp

En el componente de proveedor de ejemplo, un ejemplo de código del analizador de rutas de acceso del servicio de directorio está en Parse.cpp. El analizador de rutas de acceso es un componente clave en los componentes del proveedor de ADs. Comprueba la validez sintáctica de una ruta de acceso de ADs pasada a este proveedor. Si la sintaxis es válida, se construye una estructura **OBJECTINFO,** que contiene una versión con componentes de ADspath para este objeto.

Tenga en cuenta que se trata solo de una comprobación de sintaxis. En lugar de casos especiales cada nueva iteración de ruta de acceso, todas las comprobaciones de ruta de acceso deben cumplir las reglas de gramática establecidas por el analizador.

En la tabla siguiente se enumeran las funciones y métodos implementados en Parse.cpp.



| Elemento                      | Descripción                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analiza la ruta de acceso de ADspath que se le ha pasado. Esta función sigue las siguientes reglas gramaticales: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analiza las siguientes reglas de gramática: <SampleDSObject> -> " \\ \\ " " <identifier> \\ "<Pathname><br/>                                            |
| **ProviderName**          | Agrega el nombre del proveedor sintácticamente correcto si no existe.                                                                                                          |
| **PathName**              | Analiza las siguientes reglas gramaticales: <Pathname>  ->  <Component> " \\ \\ " <Pathname> OR<br/> <Pathname> -> <Component><br/> |
| **Componente**             | Analiza las siguientes reglas gramaticales: <Identifier> OR<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Constructor estándar.                                                                                                                                                  |
| **CLexer::~CLexer**       | Destructor estándar.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera el siguiente carácter individual.                                                                                                                                       |
| **CLexer::P ushBackToken** | Hace una copia de seguridad al principio del último token.                                                                                                                               |
| **CLexer::P ushbackChar**  | Hace una copia de seguridad de un carácter.                                                                                                                                                |
| **CLexer::IsKeyword**     | Comprueba la lista de palabras clave. Se define en Globals.h).                                                                                                                          |
| **AddComponent**          | Agrega este componente a la matriz de componentes.                                                                                                                            |
| **AddProviderName**       | Agrega un nombre de proveedor sintácticamente correcto a la **estructura OBJECTINFO.**                                                                                            |
| **AddRootRDN**            | Agrega el nombre distintivo relativo (RDN) raíz sintácticamente correcto a la **estructura OBJECTINFO.**                                                            |
| **SetType**               | Establece el tipo del objeto.                                                                                                                                           |
| **Tipo**                  | Analiza type-> "user" \| "group" y así sucesivamente.                                                                                                                          |



 

 

 





