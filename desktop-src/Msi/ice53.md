---
description: ICE53 comprueba las entradas de la tabla registro que escriben información privada del instalador o valores de directiva en el registro del sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d1e661eb832439a9b4fde423e005dc4b3a0c3ca9b266045c0ddd04daa63f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635136"
---
# <a name="ice53"></a>ICE53

ICE53 comprueba las entradas de la tabla registro que escriben información privada del instalador o valores de directiva en el registro del sistema.

## <a name="result"></a>Resultado

ICE53 envía una advertencia si la tabla del Registro especifica la escritura de información interna o de directiva en el registro.

## <a name="example"></a>Ejemplo

ICE53 publica la advertencia siguiente para el ejemplo mostrado.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Tabla del Registro](registry-table.md) (parcial)



| Registro             | Root         | Key                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ **Directivas** \\ **Microsoft** \\ **Windows** \\ **Instalador** \\ **DisableRollback**<br/> |



 

La fila de tabla del Registro "Registry1" escribe un valor de directiva del sistema en el Registro que afecta a la instalación de todos los paquetes. En función del paquete, puede ser posible deshabilitar la reversión solo para este paquete estableciendo la propiedad [**DISABLEROLLBACK**](-disablerollback.md) en la [tabla Property](property-table.md). Vea [Instalación de reversión.](rollback-installation.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




