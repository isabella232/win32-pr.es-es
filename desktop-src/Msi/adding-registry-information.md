---
description: La tabla Registro y las tablas relacionadas de la base de datos de instalación contiene la información del Registro que la aplicación necesita escribir en el registro del sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Agregar información del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb299116b4e5c567d1e1f4b18f23c1e5b0447fe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159199"
---
# <a name="adding-registry-information"></a>Agregar información del Registro

La [tabla del Registro](registry-table.md)y las tablas relacionadas de la base de datos de instalación contiene la información del Registro que la aplicación necesita escrita en el registro del sistema. Vea el grupo [Tablas del Registro](registry-tables-group.md). En esta sección agregará la información que se va a registrar en el equipo del usuario mediante Bloc de notas ejemplo.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla vacía del Registro.

[Tabla del Registro](registry-table.md)



| Registro       | Root | Clave                                 | Nombre             | Value    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfCharSet        | \#0      | Bloc de notas     |
| ClipPrecision  | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfClipPrecision  | \#2      | Bloc de notas     |
| Escape     | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfFaceName       | FixedSys | Bloc de notas     |
| Cursiva         | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfItalic         | \#0      | Bloc de notas     |
| Orientación    | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfOrientation    | \#0      | Bloc de notas     |
| OutPrecision   | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfOutPrecision   | \#1      | Bloc de notas     |
| PageSettings   | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | fSavePageSetting | \#0      | Bloc de notas     |
| PitchAndFamily | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfPitchAndFamily | \#49     | Bloc de notas     |
| PointSize      | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | iPointSize       | \#120    | Bloc de notas     |
| Calidad        | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfQuality        | \#2      | Bloc de notas     |
| Tachado      | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfStrikeOut      | \#0      | Bloc de notas     |
| Peso         | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | lfWeight         | \#400    | Bloc de notas     |
| Encapsulado           | 2    | Ejemplo \\ de software de microsoft \\ Bloc de notas | fWrap            | \#0      | Bloc de notas     |



 

[Continuar](specifying-shortcuts.md)

 

 



