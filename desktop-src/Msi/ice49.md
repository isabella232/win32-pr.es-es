---
description: ICE49 comprueba las entradas predeterminadas del Registro que no son de tipo REG \_ SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074593"
---
# <a name="ice49"></a>ICE49

ICE49 comprueba las entradas predeterminadas del Registro que no son de **tipo REG \_ SZ.**

## <a name="result"></a>Resultado

ICE49 envía una advertencia si hay una entrada predeterminada del Registro que no es un **tipo \_ REG SZ.**

## <a name="example"></a>Ejemplo

ICE49 notifica la siguiente advertencia para el ejemplo mostrado.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

El valor \# '123' es un valor del Registro **DWORD.**

[Tabla del Registro](registry-table.md) (parcial)



| Registro | Nombre | Value |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Para corregir esta advertencia, cambie el valor para escribir **REG \_ SZ**.

Los componentes con **\_ SZ no REG** son válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de instrucciones condicionales](conditional-statement-syntax.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



