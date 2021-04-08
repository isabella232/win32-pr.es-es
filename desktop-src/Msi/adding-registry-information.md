---
description: La tabla del registro y las tablas relacionadas de la base de datos de instalación contiene la información del registro que la aplicación necesita escribir en el registro del sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Agregar información del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb299116b4e5c567d1e1f4b18f23c1e5b0447fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001758"
---
# <a name="adding-registry-information"></a>Agregar información del registro

La [tabla del registro](registry-table.md)y las tablas relacionadas de la base de datos de instalación contiene la información del registro que la aplicación necesita escribir en el registro del sistema. Vea el [Grupo tablas del registro](registry-tables-group.md). En esta sección, agregará la información que se va a registrar en el equipo del usuario mediante el ejemplo del Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla del Registro vacía.

[Tabla del registro](registry-table.md)



| Registro       | Root | Clave                                 | Nombre             | Value    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfCharSet        | \#0      | Bloc de notas     |
| ClipPrecision  | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfClipPrecision  | \#2      | Bloc de notas     |
| Escape     | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfFaceName       | FixedSys | Bloc de notas     |
| Cursiva         | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfItalic         | \#0      | Bloc de notas     |
| Orientación    | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfOrientation    | \#0      | Bloc de notas     |
| Desprecisión   | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfOutPrecision   | \#1      | Bloc de notas     |
| PageSettings   | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | fSavePageSetting | \#0      | Bloc de notas     |
| PitchAndFamily | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfPitchAndFamily | \#49     | Bloc de notas     |
| PointSize      | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | iPointSize       | \#120    | Bloc de notas     |
| Calidad        | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfQuality        | \#2      | Bloc de notas     |
| Tacha      | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfStrikeOut      | \#0      | Bloc de notas     |
| Peso         | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | lfWeight         | \#400    | Bloc de notas     |
| Encapsulado           | 2    | Ejemplo de SOFTWARE de \\ Bloc de notas de Microsoft \\ | fWrap            | \#0      | Bloc de notas     |



 

[Continuar](specifying-shortcuts.md)

 

 



