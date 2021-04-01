---
title: Atributos de función
description: Los atributos \ callback \ y \ local \ se pueden aplicar como atributos de función.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793383"
---
# <a name="function-attributes"></a>Atributos de función

La **\[** [**devolución de llamada**](/windows/desktop/Midl/callback) **\]** y **\[** [](/windows/desktop/Midl/local) **\]** los atributos locales se pueden aplicar como atributos de función.

Una devolución de llamada es una llamada remota entre el servidor y el cliente que se ejecuta como parte de un subproceso conceptual de ejecución única. Una devolución de llamada siempre se emite en el contexto de una llamada remota (o devolución de llamada) y la ejecuta el subproceso que emitió la llamada remota original (o devolución de llamada).

A menudo es conveniente colocar una declaración de procedimiento local en el archivo IDL, ya que se trata del lugar lógico para describir las interfaces de un paquete. El **\[** [](/windows/desktop/Midl/local) **\]** atributo local indica que una declaración de procedimiento no es realmente una función remota, sino un procedimiento local. El compilador MIDL no genera ningún código auxiliar para las funciones con el atributo **\[ local \]** .

Es importante tener en cuenta que no se recomienda el uso de la **\[** [**devolución de llamada**](/windows/desktop/Midl/callback) **\]** en la programación multiproceso. Como función de programación de un solo subproceso, no está equipada para admitir las demandas de seguridad que proporciona un entorno con varios subprocesos.

 

 