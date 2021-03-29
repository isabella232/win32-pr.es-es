---
description: En esta sección se describen las estructuras que puede usar para desarrollar analizadores. Estas estructuras las utilizan las funciones que puede usar para desarrollar analizadores y funciones que puede usar para desarrollar analizadores o expertos.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Estructuras de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003215"
---
# <a name="parser-structures"></a>Estructuras de analizador

En esta sección se describen las estructuras que puede usar para desarrollar analizadores. Estas estructuras las utilizan las funciones que puede usar para desarrollar analizadores y funciones que puede usar para desarrollar analizadores o expertos.



| Estructura                                 | Descripción                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Define los protocolos iniciales que se usan con más frecuencia.                                                                               |
| [ENTRYPOINTS](entrypoints.md)            | Especifica punteros a los puntos de entrada de la DLL del analizador.                                                                      |
| [PF \_ FOLLOWENTRY](pf-followentry.md)     | Especifica el protocolo que sigue al protocolo actual.                                                                       |
| [PF \_ FOLLOWSET](pf-followset.md)         | Especifica el conjunto de protocolos que sigue el protocolo actual.                                                               |
| [PF \_ HANDOFFENTRY](pf-handoffentry.md)   | Especifica el protocolo que se entrega en el protocolo actual o el protocolo al que el protocolo actual se entrega.    |
| [PF \_ HANDOFFSET](pf-handoffset.md)       | Especifica el conjunto de protocolos que se entregan al protocolo actual o al conjunto de protocolos al que el protocolo actual se entrega. |
| [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) | Especifica el número de analizadores en el archivo DLL del analizador e información sobre cada analizador.                                            |
| [PF \_ PARSERINFO](pf-parserinfo.md)       | Especifica información sobre un analizador específico.                                                                                  |
| [BIT con etiqueta \_](labeled-bit.md)           | Especifica los identificadores, los campos de bits o las marcas.                                                                                        |
| [BYTE con etiqueta \_](labeled-byte.md)         | Especifica un par de etiqueta de **bytes** .                                                                                                |
| [DWORD con etiqueta \_](labeled-dword.md)       | Especifica un par de etiquetas **DWORD** .                                                                                               |
| [palabra con etiqueta \_](labeled-word.md)         | Especifica un par de etiqueta de **palabra** .                                                                                                |
| [PROPERTYINFO](propertyinfo.md)          | Especifica las propiedades que el analizador de protocolo requiere para describir los fotogramas.                                                  |
| [PROPERTYINST](propertyinst.md)          | Especifica una instancia de una propiedad en un marco.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Especifica una instancia de propiedad extendida de forma libre.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Especifica un protocolo.                                                                                                           |
| [VARIEDAD](range.md)                        | Especifica un intervalo para un número.                                                                                                 |
| [SET](set.md)                            | Especifica una tabla de valores para una propiedad.                                                                                     |



 

Para obtener información acerca de las funciones utilizadas para desarrollar archivos dll de analizador, vea los temas siguientes.



| Para información acerca de                                         | Vea                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones que exportan los archivos DLL del analizador.                        | [Funciones de exportación de DLL de analizador](parser-dll-export-functions.md)               |
| Funciones que se pueden usar para desarrollar archivos dll de analizador.            | [Funciones de analizador](parser-functions.md)                                     |
| Funciones que puede usar para desarrollar archivos dll de analizador y expertos. | [Funciones comunes de experto y analizador](expert-and-parser-common-functions.md) |



 

 

 



