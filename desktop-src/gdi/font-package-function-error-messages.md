---
description: Mensajes de error de la función de paquete de fuentes
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Mensajes de error de la función de paquete de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bcf84f92b60351e8375df682de0c3b01c2aa1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155616"
---
# <a name="font-package-function-error-messages"></a>Mensajes de error de la función de paquete de fuentes

Los siguientes valores LONG son devueltos por las funciones de paquete de fuentes ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) y [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) cuando se producen errores. Cuando las funciones se ejecutan correctamente, \_ se devuelve el valor no error.



| Valor devuelto                   | Value | Descripción                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| SIN \_ errores                      | 0     | No se ha producido ningún error.                                                                                               |
| formato de ERR \_                    | 1006  | Error de formato de datos de entrada.                                                                             |
| ERR ( \_ genérico)                   | 1000  | Se produjo un error en el código genérico.                                                                               |
| memoria de ERR \_                       | 1005  | Se produjo un error durante la asignación de memoria.                                                                      |
| ERR \_ no \_ Glyphs                | 1009  | No se encontró ningún glifo.                                                                                            |
| ERROR \_ de \_ base no válida             | 1085  | La fuente contenía una tabla de datos de línea de base (BASE) no válida. Actualmente no se usa este valor.                      |
| ERROR \_ de \_ CMAP no válido             | 1030  | La fuente contenía una tabla de asignación de caracteres a glifo (CMAP) no válida.                                           |
| ERROR \_ de \_ formato Delta no válido \_    | 1013  | Se detectó un formato Delta no válido al intentar subconjunto de una fuente Format 1 o 2.                                |
| ERROR \_ de \_ EBLC no válido             | 1086  | La fuente contenía una tabla de datos de ubicación de mapas de bits incrustada (EBLC) no válida.                                        |
| ERROR \_ de \_ GLYF no válido             | 1061  | La fuente contenía una tabla de datos de glifo (glyf) no válida.                                                           |
| ERROR \_ de \_ GDEF no válido             | 1083  | La fuente contenía una tabla de datos de definición de glifo (GDEF) no válida. Actualmente no se usa este valor.              |
| ERR \_ GPO no válidos \_             | 1082  | La fuente contenía una tabla de datos de posicionamiento de glifo (GPO) no válida. Actualmente no se usa este valor.             |
| ERROR \_ de \_ GSUB no válido             | 1081  | La fuente contenía una tabla de datos de sustitución del glifo (GSUB) no válida.                                              |
| ERROR \_ de \_ HDMX no válido             | 1089  | La fuente contenía una tabla de métricas de dispositivo horizontal (hdmx) no válida.                                            |
| ERR \_ encabezado no válido \_             | 1062  | La fuente contenía una tabla de encabezado de fuente (Head) no válida.                                                          |
| ERROR \_ de \_ HHEA no válido             | 1063  | La fuente contenía una tabla de encabezado horizontal (hhea) no válida.                                                    |
| ERROR \_ \_ de HHEA \_ o \_ VHEA no válidos   | 1072  | La fuente contenía una tabla de encabezado horizontal (hhea) no válida o una tabla de encabezado de métricas verticales (vhea) no válida. |
| ERROR \_ de \_ HMTX no válido             | 1064  | La fuente contenía una tabla de métricas horizontales (hmtx) no válida.                                                   |
| ERROR \_ \_ de HMTX \_ o \_ VMTX no válidos   | 1073  | La fuente contenía una tabla de métricas horizontales (hmtx) o una tabla de métricas verticales no válidas (vmtx).       |
| ERROR \_ de \_ JSTF no válido             | 1084  | La fuente contenía una tabla de datos de justificación (JSTF) no válida.                                                   |
| ERROR \_ de \_ LTSH no válido             | 1087  | La fuente contenía una tabla de datos de umbral lineal (LTSH) no válida.                                                |
| ERROR \_ de \_ para no válido              | 1080  | La fuente era una fuente de tipo TrueType no válida.                                                                      |
| ERROR \_ de \_ VDMX no válido             | 1088  | La fuente contenía una tabla de métricas de dispositivo vertical (VDMX) no válida.                                              |
| ERR \_ no válida de la \_             | 1065  | La fuente contenía una tabla de índice de ubicación (loca) no válida.                                                    |
| ERROR \_ de \_ MAXP no válido             | 1066  | La fuente contenía una tabla de perfil máximo (MaxP) no válida.                                                      |
| ERROR \_ de \_ sumas de comprobación de fusión mediante combinación no válida \_ | 1011  | No se ha podido realizar una combinación de sumas de comprobación para dos fuentes de una fuente de la madre diferente.                       |
| ERR \_ \_ formatos de combinación no válidos \_   | 1010  | No se pudo fusionar mediante combinación fuentes con formatos de dttf erróneos.                                          |
| ERR \_ \_ NUMGLYPHS Merge no válida \_ | 1012  | No se pudo combinar el número de glifos de dos fuentes de una fuente madre diferente.            |
| ERROR \_ de \_ nombre no válido             | 1067  | El nombre del paquete de fuentes o un nombre de fuente no era válido.                                                                |
| ERROR \_ de \_ post no válido             | 1068  | La fuente contenía una tabla de información PostScript (post) no válida.                                               |
| ERROR \_ OS2 no válido \_              | 1069  | La fuente contenía un SO/2 no válido y una tabla de métricas específicas de Windows (OS/2).                                    |
| ERROR \_ de \_ VHEA no válido             | 1070  | La fuente contenía una tabla de encabezado de métricas verticales (vhea) no válida.                                              |
| ERROR \_ de \_ VMTX no válido             | 1071  | La fuente contenía una tabla de métricas verticales no válida (vmtx).                                                     |
| ERROR \_ de \_ Índice TTC no válido \_       | 1015  | Se pasó un índice de base cero (TTC) no válido en el archivo de fuente.                                                 |
| no se encuentra un error de \_ \_ CMAP             | 1030  | La fuente no contenía una tabla CMAP.                                                                           |
| ERROR \_ de \_ EBDT que falta             | 1044  | La fuente no contenía una tabla EBDT.                                                                          |
| ERROR \_ de \_ GLYF que falta             | 1031  | La fuente no contenía una tabla glyf.                                                                           |
| \_falta el \_ encabezado de Err             | 1032  | La fuente no contenía una tabla de encabezado.                                                                           |
| ERROR \_ de \_ HHEA que falta             | 3082  | La fuente no contenía una tabla hhea.                                                                          |
| ERROR \_ de \_ HMTX que falta             | 1034  | La fuente no contenía una tabla hmtx.                                                                          |
| ERROR en la falta de la \_ \_             | 1035  | La fuente no contenía una tabla de la.                                                                           |
| ERROR \_ de \_ MAXP que falta             | 1036  | La fuente no contenía una tabla Maxp.                                                                           |
| \_falta \_ el nombre de Err             | 1037  | La fuente no contenía una tabla de nombres (nombre).                                                                  |
| \_falta \_ post en Err             | 1038  | La fuente no contenía una tabla post.                                                                           |
| \_Falta \_ OS2 en el Err              | 1039  | La fuente no contenía una tabla de SO/2.                                                                          |
| ERROR \_ de \_ VHEA que falta             | 1040  | La fuente no contenía una tabla vhea.                                                                           |
| ERROR \_ de \_ VMTX que falta             | 1041  | La fuente no contenía una tabla vmtx.                                                                           |
| \_no se encuentra \_ HHEA \_ o \_ VHEA   | 1042  | La fuente no contenía una tabla hhea o una tabla vhea.                                                          |
| \_no se encuentra \_ HMTX \_ o \_ VMTX   | 1043  | La fuente no contenía una tabla hmtx o una tabla vmtx.                                                          |
| ERROR \_ no \_ TTC                  | 1014  | El valor proporcionado no es un índice para un archivo TTC.                                                              |
| ERR \_ PARAMETER0                | 1100  | La llamada al parámetro 0 de la función no era válida.                                                                        |
| ERR \_ parámetro1                | 1101  | La llamada al parámetro 1 de la función no era válida.                                                                        |
| ERROR \_ parámetro2                | 1102  | El parámetro de función 2 de llamada no era válido.                                                                        |
| ERROR de \_ parámetro3                | 1103  | El parámetro de función 3 de llamada no era válido.                                                                        |
| ERROR de \_ parámetro4                | 1104  | El parámetro de función 4 de llamada no era válido.                                                                        |
| ERR \_ PARAMETER5                | 1105  | El parámetro de función 5 de llamada no era válido.                                                                        |
| ERR \_ PARAMETER6                | 1106  | La llamada al parámetro 6 de la función no era válida.                                                                        |
| ERR \_ PARAMETER7                | 1107  | El parámetro de función 7 de llamada no era válido.                                                                        |
| ERR \_ PARAMETER8                | 1108  | El parámetro de función 8 de llamada no era válido.                                                                        |
| ERR \_ PARAMETER9                | 1109  | El parámetro de función 9 de llamada no era válido.                                                                        |
| ERR \_ PARAMETER10               | 1110  | El parámetro de función 10 de llamada no era válido.                                                                       |
| ERR \_ PARAMETER11               | 1111  | El parámetro de función 11 de llamada no era válido.                                                                       |
| ERR \_ PARAMETER12               | 1112  | El parámetro de función 12 de llamada no era válido.                                                                       |
| ERR \_ PARAMETER13               | 1113  | La llamada al parámetro de función 13 no era válida.                                                                       |
| ERR \_ PARAMETER14               | 1114  | El parámetro de función 14 de llamada no era válido.                                                                       |
| ERR \_ PARAMETER15               | 1115  | La llamada al parámetro de función 15 no era válida.                                                                       |
| ERR \_ PARAMETER16               | 1116  | El parámetro de función 16 de llamada no era válido.                                                                       |
| ERR \_ READCONTROL               | 1003  | La estructura de control de lectura no coincidía con los datos.                                                                   |
| ERR \_ READOUTOFBOUNDS           | 1001  | No se permitió leer de la memoria, posiblemente porque los datos estaban fuera de los límites o están dañados.                          |
| versión de ERR \_                   | 1008  | El valor principal de dttf. version de los datos de entrada era mayor que la versión que la función puede leer.                   |
| el \_ error \_ aumentaría               | 1007  | La acción solicitada provocó el crecimiento de los datos y la aplicación debe usar los datos originales.                             |
| ERR \_ WRITECONTROL              | 1004  | La estructura de control de escritura no coincidía con los datos.                                                                  |
| ERR \_ WRITEOUTOFBOUNDS          | 1002  | No se permitió escribir en la memoria, posiblemente porque los datos estaban fuera de los límites.                                      |



 

 

 



