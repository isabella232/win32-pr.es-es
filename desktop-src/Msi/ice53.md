---
description: ICE53 comprueba las entradas de la tabla registro que escriben información privada del instalador o valores de directiva en el registro del sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074588"
---
# <a name="ice53"></a>ICE53

ICE53 comprueba las entradas de la tabla registro que escriben información privada del instalador o valores de directiva en el registro del sistema.

## <a name="result"></a>Resultado

ICE53 envía una advertencia si la tabla del Registro especifica la escritura de información interna o de directiva en el registro.

## <a name="example"></a>Ejemplo

ICE53 publica la siguiente advertencia para el ejemplo mostrado.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Tabla del Registro](registry-table.md) (parcial)



| Registro             | Root         | Clave                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ **Directivas** \\ **Microsoft** \\ **Windows** \\ **Instalador** \\ **DisableRollback**<br/> |



 

La fila de tabla del Registro "Registry1" escribe un valor de directiva del sistema en el Registro que afecta a la instalación de todos los paquetes. En función del paquete, puede ser posible deshabilitar la reversión solo para este paquete estableciendo la propiedad [**DISABLEROLLBACK**](-disablerollback.md) en la [tabla Property](property-table.md). Vea [Instalación de reversión.](rollback-installation.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




