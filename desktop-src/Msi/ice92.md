---
description: ICE92 comprueba que un componente sin un GUID de identificador de componente no se especifica también como un componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910706"
---
# <a name="ice92"></a>ICE92

ICE92 comprueba que un componente sin un GUID de identificador de componente no se especifica también como un componente permanente. Esta acción personalizada de ICE comprueba la [tabla](component-table.md) de componentes en busca de componentes sin un [GUID](guid.md) especificado en el campo ComponentID y comprueba que la marca **msidbComponentAttributesPermanent** no se ha establecido en el campo atributos. ICE92 también comprueba que ningún componente tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence** .

Si la columna ComponentId es null, el instalador no registra el componente y el instalador no puede quitarlo ni repararlo.

## <a name="result"></a>Resultado

ICE92 expone el siguiente error.



| Error ICE92                                                          | Descripción                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El componente ' \[ 1 \] ' no tiene ningún ComponentID y está marcado como permanente. | La entrada de este componente en la tabla componente tiene el valor null en la columna ComponentId y tiene **msidbComponentAttributesPermanent** en la columna Attributes. |



 

ICE92 envía la siguiente advertencia.



| ADVERTENCIA de ICE92                                                                                                                                                           | Descripción                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El componente ' \[ 1 \] ' está marcado como Permanent y Uninstall-on-subestado. Se omitirá el atributo Uninstall-on-sustitución porque el componente es permanente. | La entrada de este componente en la [tabla de componentes](component-table.md) tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence** especificados. |



 

## <a name="example"></a>Ejemplo

ICE92 notifica el siguiente error para el ejemplo:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Tabla de componentes](component-table.md) (parcial)



| Componente  | ComponentId | Directorio\_ | Atributos | Rutas |
|------------|-------------|-------------|------------|---------|
| Component1 |             | Directorioa  | 16         | Archivoa   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



