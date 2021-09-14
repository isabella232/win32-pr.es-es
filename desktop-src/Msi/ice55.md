---
description: ICE55 valida que todos los objetos LockPermission existen y tienen valores de permiso válidos.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074583"
---
# <a name="ice55"></a>ICE55

ICE55 valida que todos los objetos LockPermission existen y tienen valores de permiso válidos.

## <a name="result"></a>Resultado

ICE55 publica un error si no existe un LockObject enumerado en la tabla [LockPermissions](lockpermissions-table.md) o si no se especifica ningún nivel de privilegio en la columna Permission.

## <a name="example"></a>Ejemplo

ICE55 notificaría los siguientes errores para el ejemplo.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Tabla LockPermissions](lockpermissions-table.md) (parcial)



| LockObject | Tabla | Domain | Usuario  | Permiso |
|------------|-------|--------|-------|------------|
| Archivo1      | Archivo  |        | guest |            |
| File3      | Archivo  |        | guest | 1          |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Versión | Idioma |
|-------|---------|----------|
| Archivo1 | Archivo2   |          |
| Archivo2 | 1.0.0.0 | 3082     |



 

El objeto File1 tiene un valor NULL en la columna Permission . Cada fila debe tener un valor en la columna Permisos. Para corregir este error, especifique un valor numérico en esta columna. Si no se necesitan privilegios para este objeto, debe quitar la fila.

El objeto File3 descrito en la tabla LockPermissions no aparece en la tabla File. Para corregir este error, consulte un objeto válido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



