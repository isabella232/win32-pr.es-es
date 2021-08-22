---
description: ICE42 valida que los servidores InProc no están vinculados a archivos EXE en la tabla Class. También valida que solo las clases LocalServer y LocalServer32 tienen argumentos y valores DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b913b92d82ad25a9722b289596f6b51940bbade55b5e544ebf636051e21b3ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581075"
---
# <a name="ice42"></a>ICE42

ICE42 valida que los servidores InProc no están vinculados a archivos EXE en la [tabla Class](class-table.md). También valida que solo las clases LocalServer y LocalServer32 tienen argumentos y valores DefInProc.

## <a name="result"></a>Resultado

ICE42 genera un error si hay servidores InProc vinculados a archivos EXE en la tabla Class.

## <a name="example"></a>Ejemplo

ICE42 notificaría los errores siguientes para el ejemplo mostrado.



| Error ICE42                                                                                                                             | Descripción                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID '{GUID1}' es un servidor InProc, pero el componente de implementación 'Component1' tiene un EXE ('test.exe') como keyFile.                | Hay un archivo ejecutable especificado como servidor InProc. Los archivos EXE no pueden ser servidores InProc.                                                                                                                            |
| CLSID "{GUID1}" en el contexto "InProcServer32" tiene un argumento . Solo los contextos LocalServer pueden tener argumentos.                              | Para corregir este error, quite el argumento .                                                                                                                                                                                   |
| CLSID "{GUID1}" en el contexto "InProcServer32" especifica un valor InProc predeterminado. Solo los contextos LocalServer pueden tener valores InProc predeterminados. | Hay un objeto con un valor InProc predeterminado que no es un objeto que funciona en los contextos LocalServer o LocalServer32. Para corregir este error, quite el valor DeflnProc o cambie el contexto de la clase .<br/> |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID   | Context        | Componente\_ | DefInProcHandler | Argumento |
|---------|----------------|-------------|------------------|----------|
| {GUID1} | InProcServer32 | Componente1  | InProcServer     | Arg      |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | KeyPath |
|------------|---------|
| Componente1 | Archivo1   |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Nombre de archivo |
|-------|----------|
| Archivo1 | test.exe |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




