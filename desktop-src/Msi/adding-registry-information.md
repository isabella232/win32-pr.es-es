---
description: La tabla Registro y las tablas relacionadas de la base de datos de instalación contiene la información del Registro que la aplicación necesita escribir en el registro del sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Agregar información del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df31ad20fef317d5d67f7f45a7b877511d4c35b05b1517c529693e787306b44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066415"
---
# <a name="adding-registry-information"></a>Agregar información del Registro

La [tabla del Registro](registry-table.md)y las tablas relacionadas de la base de datos de instalación contiene la información del Registro que la aplicación necesita escrita en el registro del sistema. Vea el grupo [Tablas del Registro](registry-tables-group.md). En esta sección agregará la información que se va a registrar en el equipo del usuario mediante el Bloc de notas ejemplo.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla vacía del Registro.

[Tabla del Registro](registry-table.md)



| Registro       | Root | Clave                                 | Nombre             | Valor    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfCharSet        | \#0      | Bloc de notas     |
| ClipPrecision  | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfClipPrecision  | \#2      | Bloc de notas     |
| Escape     | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfFaceName       | FixedSys | Bloc de notas     |
| Cursiva         | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfItalic         | \#0      | Bloc de notas     |
| Orientación    | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfOrientation    | \#0      | Bloc de notas     |
| OutPrecision   | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfOutPrecision   | \#1      | Bloc de notas     |
| PageSettings   | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | fSavePageSetting | \#0      | Bloc de notas     |
| PitchAndFamily | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfPitchAndFamily | \#49     | Bloc de notas     |
| PointSize      | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | iPointSize       | \#120    | Bloc de notas     |
| Calidad        | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfQuality        | \#2      | Bloc de notas     |
| Tachado      | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfStrikeOut      | \#0      | Bloc de notas     |
| Peso         | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | lfWeight         | \#400    | Bloc de notas     |
| Encapsulado           | 2    | SOFTWARE \\ Microsoft \\ Bloc de notas Sample | fWrap            | \#0      | Bloc de notas     |



 

[Continuar](specifying-shortcuts.md)

 

 



