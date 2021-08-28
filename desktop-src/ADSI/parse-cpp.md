---
title: ANALIZAR. CPP
description: En el componente de proveedor de ejemplo, un ejemplo de código del analizador de rutas de acceso del servicio de directorio se encuentra en Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- parse.cpp ADSI
- ADSI del analizador de rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518db6857f9b7018a0dbf3e1e97ac60ed654447d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880286"
---
# <a name="parsecpp"></a>ANALIZAR. CPP

En el componente de proveedor de ejemplo, un ejemplo de código del analizador de rutas de acceso del servicio de directorio se encuentra en Parse.cpp. El analizador de rutas de acceso es un componente clave en los componentes del proveedor de ADs. Comprueba la validez sintáctica de una ruta de acceso de ADs pasada a este proveedor. Si la sintaxis es válida, se construye una estructura **OBJECTINFO,** que contiene una versión con componentes de ADspath para este objeto.

Tenga en cuenta que se trata solo de una comprobación de sintaxis. En lugar de casos especiales cada nueva iteración de ruta de acceso, toda comprobación de la ruta de acceso debe cumplir las reglas de gramática establecidas por el analizador.

En la tabla siguiente se enumeran las funciones y métodos implementados en Parse.cpp.



| Elemento                      | Descripción                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analiza la ruta de acceso de ADspath que se le ha pasado. Esta función sigue las siguientes reglas de gramática: &lt; ADsObject &gt;  ->  &lt; ProviderName &gt; &lt; SampleDSObject&gt;<br/>     |
| **SampleDSObject**        | Analiza las siguientes reglas de gramática: &lt; SampleDSObject &gt; -> \\ \\ " " identifier " &lt; " &gt; \\ &lt; Pathname&gt;<br/>                                            |
| **ProviderName**          | Agrega el nombre del proveedor sintácticamente correcto si no existe.                                                                                                          |
| **PathName**              | Analiza las siguientes reglas de gramática: &lt; Pathname &gt;  ->  &lt; Component " &gt; " \\ \\ &lt; Pathname &gt; OR<br/> &lt;Pathname &gt;  ->  &lt; (Componente)&gt;<br/> |
| **Componente**             | Analiza las siguientes reglas gramaticales: &lt; Identificador &gt; OR<br/> &lt;Identificador &gt; "=" &lt; Identificador&gt;<br/>                                              |
| **CLexer::CLexer**        | Constructor estándar.                                                                                                                                                  |
| **CLexer::~CLexer**       | Destructor estándar.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera el siguiente carácter individual.                                                                                                                                       |
| **CLexer::P ushBackToken** | Hace una copia de seguridad al principio del último token.                                                                                                                               |
| **CLexer::P ushbackChar**  | Hace una copia de seguridad de un carácter.                                                                                                                                                |
| **CLexer::IsKeyword**     | Comprueba la lista de palabras clave. Definido en Globals.h).                                                                                                                          |
| **AddComponent**          | Agrega este componente a la matriz de componentes.                                                                                                                            |
| **AddProviderName**       | Agrega un nombre de proveedor sintácticamente correcto a la **estructura OBJECTINFO.**                                                                                            |
| **AddRootRDN**            | Agrega el nombre distintivo relativo (RDN) raíz sintácticamente correcto a la **estructura OBJECTINFO.**                                                            |
| **SetType**               | Establece el tipo del objeto.                                                                                                                                           |
| **Tipo**                  | Analiza type-> "user" \| "group" y así sucesivamente.                                                                                                                          |



 

 

 





