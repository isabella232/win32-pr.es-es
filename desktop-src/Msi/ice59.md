---
description: ICE59 comprueba que los accesos directos anunciados pertenecen a los componentes que se instalan con la característica de destino del acceso directo.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652589"
---
# <a name="ice59"></a>ICE59

ICE59 comprueba que los accesos directos anunciados pertenecen a los componentes que se instalan con la característica de destino del acceso directo.

Los errores informados por ICE59 generalmente conducen al comportamiento siguiente:

1.  El acceso directo anunciado iniciará el Windows Installer para instalar la característica que se muestra en la columna destino.
2.  Pero como la [tabla FeatureComponents](featurecomponents-table.md) no asigna la característica de destino al componente que contiene el acceso directo, el keyfile del componente (que se activa mediante el acceso directo) no está instalado.
3.  Por lo tanto, el acceso directo se rompe y no hará nada.

## <a name="result"></a>Resultado

ICE59 publica un error si un acceso directo anunciado no pertenece a los componentes que se instalan con la característica de destino del acceso directo.

## <a name="example"></a>Ejemplo

ICE59 notifica el siguiente error para el ejemplo mostrado:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

En este caso, ShortcutB anuncia Featurea y, cuando se activa, inicia el archivo de clave de ComponentB. Además, ComponentB nunca se instala con Featurea, por lo que, incluso después de que se complete la fase de instalación a petición, el destino del acceso directo no existe.

Para corregir este error, agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que asocia featurea y ComponentB.

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Destino   | Componente\_ |
|-----------|----------|-------------|
| ShortcutB | FeatureA | ComponentB  |



 

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| FeatureA  | Componentea  |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  | Nivel |
|----------|-------|
| FeatureA | 10    |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Rutas |
|------------|---------|
| Componentea | Archivoa   |
| ComponentB | FileB   |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | Secuencia |
|-------|-------------|----------|
| Archivoa | Componentea  | 1        |
| FileB | ComponentB  | 2        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



