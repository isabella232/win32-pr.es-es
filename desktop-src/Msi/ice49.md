---
description: ICE49 comprueba las entradas del Registro predeterminadas que no son del \_ tipo REG SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911913"
---
# <a name="ice49"></a>ICE49

ICE49 comprueba las entradas del Registro predeterminadas que no son del tipo **reg \_ SZ** .

## <a name="result"></a>Resultado

ICE49 publica una advertencia si hay una entrada del registro predeterminada que no es un **tipo \_ de reg** .

## <a name="example"></a>Ejemplo

ICE49 notifica la siguiente advertencia para el ejemplo que se muestra.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

El valor ' \# 123 ' es un valor del registro **DWORD** .

[Tabla del registro](registry-table.md) (parcial)



| Registro | Nombre | Value |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Para corregir esta advertencia, cambie el valor a tipo **reg \_ SZ**.

Los componentes que no son de **reg \_** son válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



