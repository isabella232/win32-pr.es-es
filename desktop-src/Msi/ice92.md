---
description: ICE92 comprueba que un componente sin un GUID de identificador de componente no se especifica también como componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074510"
---
# <a name="ice92"></a>ICE92

ICE92 comprueba que un componente sin un GUID de identificador de componente no se especifica también como componente permanente. Esta acción personalizada [](component-table.md) de ICE comprueba los componentes de la tabla de componentes sin un [GUID](guid.md) especificado en el campo ComponentId y comprueba que la marca **msidbComponentAttributesPermanent** no se ha establecido en el campo Atributos. ICE92 también comprueba que ningún componente tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence.**

Si la columna ComponentId es NULL, el instalador no registra el componente y el instalador no puede quitarlo ni repararlo.

## <a name="result"></a>Resultado

ICE92 publica el siguiente error.



| Error ice92                                                          | Descripción                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El componente ' \[ 1 \] ' no tiene componentId y está marcado como permanente. | La entrada de este componente en la tabla Component tiene null en la columna ComponentId y **tiene msidbComponentAttributesPermanent** en la columna Attributes. |



 

ICE92 publica la advertencia siguiente.



| Advertencia de ICE92                                                                                                                                                           | Descripción                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El componente ' \[ 1 \] ' está marcado como permanente y desinstalación tras sustitución. El atributo uninstall-on-supersedence se omitirá porque el componente es permanente. | La entrada de este componente en la tabla [Component](component-table.md) tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence** especificados. |



 

## <a name="example"></a>Ejemplo

ICE92 notifica el siguiente error para el ejemplo:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Componentid | Directorio\_ | Atributos | KeyPath |
|------------|-------------|-------------|------------|---------|
| Componente1 |             | DirectorioA  | 16         | ArchivoA   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



