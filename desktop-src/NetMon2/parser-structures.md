---
description: En esta sección se describen las estructuras que puede usar para desarrollar analizadores. Estas estructuras las usan las funciones que puede usar para desarrollar analizadores y funciones que puede usar para desarrollar analizadores o expertos.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Estructuras del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d54e02e26e9874f27f49312a84b4b643cc4b3bfdb0c6056f274e4febecf0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082535"
---
# <a name="parser-structures"></a>Estructuras del analizador

En esta sección se describen las estructuras que puede usar para desarrollar analizadores. Estas estructuras las usan las funciones que puede usar para desarrollar analizadores y funciones que puede usar para desarrollar analizadores o expertos.



| Estructura                                 | Descripción                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Define los protocolos iniciales más usados.                                                                               |
| [ENTRYPOINTS](entrypoints.md)            | Especifica punteros a los puntos de entrada para el archivo DLL del analizador.                                                                      |
| [PF \_ FOLLOWENTRY](pf-followentry.md)     | Especifica el protocolo que sigue al protocolo actual.                                                                       |
| [PF \_ FOLLOWSET](pf-followset.md)         | Especifica el conjunto de protocolos que sigue al protocolo actual.                                                               |
| [PF \_ HANDOFFENTRY](pf-handoffentry.md)   | Especifica el protocolo que se entrega al protocolo actual o el protocolo al que se entrega el protocolo actual.    |
| [PF \_ HANDOFFSET](pf-handoffset.md)       | Especifica el conjunto de protocolos que se entregan al protocolo actual o al conjunto de protocolos al que se entrega el protocolo actual. |
| [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) | Especifica el número de analizadores del archivo DLL del analizador e información sobre cada analizador.                                            |
| [PF \_ PARSERINFO](pf-parserinfo.md)       | Especifica información sobre un analizador específico.                                                                                  |
| [BIT \_ ETIQUETADO](labeled-bit.md)           | Especifica identificadores, campos BIT o marcas.                                                                                        |
| [BYTE \_ ETIQUETADO](labeled-byte.md)         | Especifica un par **de etiquetas BYTE.**                                                                                                |
| [ETIQUETADA \_ COMO DWORD](labeled-dword.md)       | Especifica un par **de etiquetas DWORD.**                                                                                               |
| [PALABRA \_ ETIQUETADA](labeled-word.md)         | Especifica un par **de etiquetas WORD.**                                                                                                |
| [Propertyinfo](propertyinfo.md)          | Especifica las propiedades que el analizador de protocolos requiere para describir fotogramas.                                                  |
| [PROPERTYINST](propertyinst.md)          | Especifica una instancia de una propiedad en un marco.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Especifica una instancia de propiedad extendida de forma libre.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Especifica un protocolo.                                                                                                           |
| [Gama](range.md)                        | Especifica un intervalo para un número.                                                                                                 |
| [SET](set.md)                            | Especifica una tabla de valores para una propiedad.                                                                                     |



 

Para obtener información sobre las funciones que se usan para desarrollar archivos DLL de analizador, vea los temas siguientes.



| Para información acerca de                                         | Vea                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones que exportan los archivos DLL del analizador.                        | [Funciones de exportación de DLL del analizador](parser-dll-export-functions.md)               |
| Funciones que puede usar para desarrollar archivos DLL de analizador.            | [Funciones del analizador](parser-functions.md)                                     |
| Funciones que puede usar para desarrollar archivos DLL expertos y analizadores. | [Funciones comunes de expertos y analizadores](expert-and-parser-common-functions.md) |



 

 

 



