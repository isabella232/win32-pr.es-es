---
title: Atributos de función
description: Los atributos \ callback\ y \ local\ se pueden aplicar como atributos de función.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361933"
---
# <a name="function-attributes"></a>Atributos de función

La **\[** [**devolución de**](/windows/desktop/Midl/callback) **\]** llamada y los atributos **\[** [**locales**](/windows/desktop/Midl/local) se pueden aplicar como **\]** atributos de función.

Una devolución de llamada es una llamada remota desde el servidor al cliente que se ejecuta como parte de un subproceso conceptual de ejecución única. Una devolución de llamada siempre se emite en el contexto de una llamada remota (o devolución de llamada) y la ejecuta el subproceso que emitió la llamada remota original (o devolución de llamada).

A menudo es conveniente colocar una declaración de procedimiento local en el archivo IDL, ya que este es el lugar lógico para describir las interfaces de un paquete. El **\[** [**atributo local**](/windows/desktop/Midl/local) **\]** indica que una declaración de procedimiento no es realmente una función remota, sino un procedimiento local. El compilador MIDL no genera ningún código auxiliar para las funciones con el **\[ atributo local. \]**

Es importante tener en cuenta que no se recomienda el uso de la **\[** [**devolución**](/windows/desktop/Midl/callback) de **\]** llamada en la programación multiproceso. Como función de programación de un solo subproceso, no está equipado para admitir las demandas de seguridad que proporciona un entorno de varios subprocesos.

 

 