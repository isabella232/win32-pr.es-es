---
description: Mensajes de error de función de paquete de fuentes
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Mensajes de error de función de paquete de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7008707675d9b2ef3eb31229535b07b1af6000e43d1122c2929fd12988fb4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761088"
---
# <a name="font-package-function-error-messages"></a>Mensajes de error de función de paquete de fuentes

Las funciones del paquete de fuentes ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) y [**MergeFontPackage)**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) devuelven los siguientes valores LONG cuando se encuentran errores. Cuando las funciones se han realizado correctamente, se devuelve el valor NO \_ ERROR.



| Valor devuelto                   | Valor | Descripción                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| NO \_ ERROR                      | 0     | No se ha producido ningún error.                                                                                               |
| FORMATO \_ ERR                    | 1006  | Error de formato de datos de entrada.                                                                             |
| ERR \_ GENERIC                   | 1000  | Error en el código genérico.                                                                               |
| ERR \_ MEM                       | 1005  | Error durante la asignación de memoria.                                                                      |
| ERR \_ NO \_ GLYPHS                | 1009  | No se encontraron glifos.                                                                                            |
| BASE \_ NO VÁLIDA DE \_ ERROR             | 1085  | La fuente contenía una tabla de datos de línea base (BASE) no válida. Actualmente no se usa este valor.                      |
| ERROR \_ INVALID \_ CMAP             | 1030  | La fuente contenía una tabla de asignación de caracteres a glifos (cmap) no válida.                                           |
| FORMATO \_ DELTA NO VÁLIDO DE \_ \_ ERROR    | 1013  | Se detectó un formato delta no válido al intentar crear un subconjunto de una fuente de formato 1 o 2.                                |
| ERR \_ INVALID \_ EBLC             | 1086  | La fuente contenía una tabla de datos de ubicación de mapa de bits incrustada (EBLC) no válida.                                        |
| ERROR \_ \_ GLYF NO VÁLIDO             | 1061  | La fuente contenía una tabla de datos de glifo no válidos (glyf).                                                           |
| ERROR \_ INVALID \_ GDEF             | 1083  | La fuente contenía una tabla de datos de definición de glifo (GDEF) no válida. Actualmente no se usa este valor.              |
| ERRORES \_ \_ GPO NO VÁLIDOS             | 1082  | La fuente contenía una tabla de datos de posición de glifo (GPOS) no válida. Actualmente no se usa este valor.             |
| ERROR \_ \_ GSUB NO VÁLIDO             | 1081  | La fuente contenía una tabla de datos de sustitución de glifos (GSUB) no válida.                                              |
| ERROR \_ \_ HDMX NO VÁLIDO             | 1089  | La fuente contenía una tabla de métricas de dispositivo horizontal (hdmx) no válida.                                            |
| ERROR \_ INVALID \_ HEAD             | 1062  | La fuente contenía una tabla de encabezado de fuente (encabezado) no válida.                                                          |
| ERROR \_ \_ HHEA NO VÁLIDO             | 1063  | La fuente contenía una tabla de encabezado horizontal (hhea) no válida.                                                    |
| ERROR \_ \_ HHEA O \_ VHEA NO \_ VÁLIDOS   | 1072  | La fuente contenía una tabla de encabezado horizontal (hhea) no válida o una tabla de encabezado de métricas verticales (vhea) no válida. |
| ERROR \_ NO VÁLIDO \_ HMTX             | 1064  | La fuente contenía una tabla de métricas horizontales (hmtx) no válida.                                                   |
| ERROR \_ NO VÁLIDO \_ HMTX O \_ \_ VMTX   | 1073  | La fuente contenía una tabla de métricas horizontales (hmtx) no válida o una tabla de métricas verticales (vmtx) no válida.       |
| ERROR \_ \_ JSTF NO VÁLIDO             | 1084  | La fuente contenía una tabla de datos de justificación no válidos (JSTF).                                                   |
| ERR \_ INVALID \_ LTSH             | 1087  | La fuente contenía una tabla de datos de umbral lineal (LTSH) no válida.                                                |
| ERROR \_ \_ TTO NO VÁLIDO              | 1080  | La fuente era una fuente TrueType Open no válida.                                                                      |
| ERROR \_ \_ VDMX NO VÁLIDO             | 1088  | La fuente contenía una tabla de métricas de dispositivo vertical (VDMX) no válida.                                              |
| ERR \_ INVALID \_ LOCA             | 1065  | La fuente contenía un índice no válido para la tabla location (loca).                                                    |
| ERROR \_ INVALID \_ MAXP             | 1066  | La fuente contenía una tabla de perfil máximo (maxp) no válida.                                                      |
| SUMAS \_ DE COMPROBACIÓN DE MEZCLA NO \_ \_ VÁLIDAS DE ERROR | 1011  | No se ha intentado combinar sumas de comprobación para dos fuentes de una fuente de madre diferente.                       |
| FORMATOS \_ DE COMBINACIÓN NO \_ VÁLIDOS DE \_ ERROR   | 1010  | No se ha intentado combinar fuentes con formatos dttf incorrectos.                                          |
| ERROR \_ NO VÁLIDO MERGE \_ \_ NUMGLYPHS | 1012  | No se ha intentado combinar el número de glifos de dos fuentes de una fuente de madre diferente.            |
| NOMBRE \_ NO VÁLIDO DE \_ ERROR             | 1067  | El nombre del paquete de fuentes o un nombre de fuente no era válido.                                                                |
| ERROR \_ POST NO \_ VÁLIDO             | 1068  | La fuente contenía una tabla de PostScript (post) no válida.                                               |
| ERROR \_ INVALID \_ OS2              | 1069  | La fuente contenía una tabla OS/2 no válida y Windows métricas específicas del sistema operativo (OS/2).                                    |
| ERROR \_ \_ VHEA NO VÁLIDO             | 1070  | La fuente contenía una tabla de encabezado de métricas verticales (vhea) no válida.                                              |
| ERROR \_ INVALID \_ VMTX             | 1071  | La fuente contenía una tabla de métricas verticales (vmtx) no válida.                                                     |
| ERROR \_ INVALID \_ TTC \_ INDEX       | 1015  | Se pasó un índice de base cero (TTC) no válido en el archivo de fuente.                                                 |
| ERROR \_ MISSING \_ CMAP             | 1030  | La fuente no contenía una tabla cmap.                                                                           |
| ERR \_ MISSING \_ EBDT             | 1044  | La fuente no contenía una tabla EBDT.                                                                          |
| ERR \_ MISSING \_ GLYF             | 1031  | La fuente no contenía una tabla glyf.                                                                           |
| ERR \_ MISSING \_ HEAD             | 1032  | La fuente no contenía una tabla principal.                                                                           |
| ERR \_ MISSING \_ HHEA             | 3082  | La fuente no contenía una tabla hhea.                                                                          |
| ERR \_ MISSING \_ HMTX             | 1034  | La fuente no contenía una tabla hmtx.                                                                          |
| ERR \_ MISSING \_ LOCA             | 1035  | La fuente no contenía una tabla loca.                                                                           |
| ERR \_ MISSING \_ MAXP             | 1036  | La fuente no contenía una tabla maxp.                                                                           |
| ERR \_ MISSING \_ NAME             | 1037  | La fuente no contenía una tabla de nomenclatura (nombre).                                                                  |
| ERROR \_ MISSING \_ POST             | 1038  | La fuente no contenía una tabla de publicación.                                                                           |
| ERR \_ MISSING \_ OS2              | 1039  | La fuente no contenía una tabla OS/2.                                                                          |
| ERR \_ MISSING \_ VHEA             | 1040  | La fuente no contenía una tabla vhea.                                                                           |
| ERROR \_ MISSING \_ VMTX             | 1041  | La fuente no contenía una tabla vmtx.                                                                           |
| ERR \_ MISSING \_ HHEA \_ OR \_ VHEA   | 1042  | La fuente no contenía una tabla hhea ni una tabla vhea.                                                          |
| ERR \_ MISSING \_ HMTX \_ OR \_ VMTX   | 1043  | La fuente no contenía una tabla hmtx ni una tabla vmtx.                                                          |
| ERR \_ NOT \_ TTC                  | 1014  | El valor proporcionado no era un índice para un archivo TTC.                                                              |
| ERR \_ PARAMETER0                | 1100  | La llamada al parámetro de función 0 no era válida.                                                                        |
| ERR \_ PARAMETER1                | 1101  | La llamada al parámetro de función 1 no era válida.                                                                        |
| ERR \_ PARAMETER2                | 1102  | La llamada al parámetro de función 2 no era válida.                                                                        |
| ERR \_ PARAMETER3                | 1103  | La llamada al parámetro de función 3 no era válida.                                                                        |
| ERR \_ PARAMETER4                | 1104  | La llamada al parámetro de función 4 no era válida.                                                                        |
| ERR \_ PARAMETER5                | 1105  | La llamada al parámetro de función 5 no era válida.                                                                        |
| ERR \_ PARAMETER6                | 1106  | La llamada al parámetro de función 6 no era válida.                                                                        |
| ERR \_ PARAMETER7                | 1107  | La llamada al parámetro de función 7 no era válida.                                                                        |
| ERR \_ PARAMETER8                | 1108  | La llamada al parámetro de función 8 no era válida.                                                                        |
| ERR \_ PARAMETER9                | 1109  | La llamada al parámetro de función 9 no era válida.                                                                        |
| ERR \_ PARAMETER10               | 1110  | La llamada al parámetro de función 10 no era válida.                                                                       |
| ERR \_ PARAMETER11               | 1111  | La llamada al parámetro de función 11 no era válida.                                                                       |
| ERR \_ PARAMETER12               | 1112  | La llamada al parámetro de función 12 no era válida.                                                                       |
| ERR \_ PARAMETER13               | 1113  | La llamada al parámetro de función 13 no era válida.                                                                       |
| ERR \_ PARAMETER14               | 1114  | La llamada al parámetro de función 14 no era válida.                                                                       |
| ERR \_ PARAMETER15               | 1115  | La llamada al parámetro de función 15 no era válida.                                                                       |
| ERR \_ PARAMETER16               | 1116  | La llamada al parámetro de función 16 no era válida.                                                                       |
| ERR \_ READCONTROL               | 1003  | La estructura del control de lectura no coincide con los datos.                                                                   |
| ERR \_ READOUTOFBOUNDS           | 1001  | No se permitió una lectura de memoria, posiblemente porque los datos están fuera de los límites o están dañados.                          |
| VERSIÓN DE \_ ERR                   | 1008  | El valor dttf.version principal de los datos de entrada era mayor que la versión que la función puede leer.                   |
| ERR \_ \_ CRECERÍA               | 1007  | La acción solicitada hizo que los datos creciera y la aplicación debe usar los datos originales.                             |
| ERR \_ WRITECONTROL              | 1004  | La estructura del control de escritura no coincide con los datos.                                                                  |
| ERR \_ WRITEOUTOFBOUNDS          | 1002  | No se permitió una escritura en la memoria, posiblemente porque los datos están fuera de los límites.                                      |



 

 

 



