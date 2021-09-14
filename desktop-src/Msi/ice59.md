---
description: ICE59 comprueba que los accesos directos anunciados pertenecen a componentes instalados por la característica de destino del acceso directo.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074574"
---
# <a name="ice59"></a>ICE59

ICE59 comprueba que los accesos directos anunciados pertenecen a componentes instalados por la característica de destino del acceso directo.

Los errores notificados por ICE59 suelen dar lugar al comportamiento siguiente:

1.  El acceso directo anunciado iniciará el instalador Windows instalar la característica que aparece en la columna Destino.
2.  Pero dado que la [tabla FeatureComponents](featurecomponents-table.md) no asigna la característica de destino al componente que contiene el acceso directo, el archivo de claves del componente (que se activa mediante el acceso directo) no está instalado.
3.  Por lo tanto, el acceso directo está roto y no hará nada.

## <a name="result"></a>Resultado

ICE59 publica un error si un acceso directo anunciado no pertenece a los componentes instalados por la característica de destino del acceso directo.

## <a name="example"></a>Ejemplo

ICE59 notifica el siguiente error para el ejemplo mostrado:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

En este caso, ShortcutB anuncia FeatureA y, cuando se activa, inicia el archivo de clave de ComponentB. Sin embargo, ComponentB nunca se instala mediante FeatureA, por lo que incluso una vez completada la fase de instalación a petición, el destino del acceso directo no existe.

Para corregir este error, agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que asocie FeatureA y ComponentB.

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Destino   | Componente\_ |
|-----------|----------|-------------|
| ShortcutB | CaracterísticaA | ComponentB  |



 

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| CaracterísticaA  | Componente A  |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  | Nivel |
|----------|-------|
| CaracterísticaA | 10    |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | KeyPath |
|------------|---------|
| Componente A | Archivo A   |
| ComponentB | FileB   |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | Secuencia |
|-------|-------------|----------|
| Archivo A | Componente A  | 1        |
| FileB | ComponentB  | 2        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



