---
description: ICE42 valida que los servidores INPROC no están vinculados a archivos EXE de la tabla de clases. También valida que solo las clases LocalServer y LocalServer32 tengan argumentos y valores DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652813"
---
# <a name="ice42"></a>ICE42

ICE42 valida que los servidores INPROC no están vinculados a archivos EXE de la [tabla de clases](class-table.md). También valida que solo las clases LocalServer y LocalServer32 tengan argumentos y valores DefInProc.

## <a name="result"></a>Resultado

ICE42 publica un error si hay servidores INPROC vinculados a archivos EXE en la tabla de clases.

## <a name="example"></a>Ejemplo

ICE42 notificaría los siguientes errores para el ejemplo que se muestra.



| Error ICE42                                                                                                                             | Descripción                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El CLSID ' {GUID1} ' es un servidor INPROC, pero el componente de implementación ' Component1 ' tiene un archivo EXE (' test.exe ') como KeyFile.                | Hay un archivo ejecutable especificado como servidor INPROC. Los archivos EXE no pueden ser servidores INPROC.                                                                                                                            |
| El CLSID ' {GUID1} ' en el contexto ' InProcServer32 ' tiene un argumento. Solo los contextos LocalServer pueden tener argumentos.                              | Para corregir este error, quite el argumento.                                                                                                                                                                                   |
| El CLSID ' {GUID1} ' en el contexto ' InProcServer32 ' especifica un valor INPROC predeterminado. Solo los contextos LocalServer pueden tener valores INPROC predeterminados. | Hay un objeto con un valor INPROC predeterminado que no es un objeto que funciona en los contextos LocalServer o LocalServer32. Para corregir este error, quite el valor DeflnProc o cambie el contexto de la clase.<br/> |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID   | Context        | Componente\_ | DefInProcHandler | Argumento |
|---------|----------------|-------------|------------------|----------|
| GUID1 | InProcServer32 | Component1  | InProcServer     | Argumento      |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Rutas |
|------------|---------|
| Component1 | Archivo1   |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Nombre de archivo |
|-------|----------|
| Archivo1 | test.exe |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




