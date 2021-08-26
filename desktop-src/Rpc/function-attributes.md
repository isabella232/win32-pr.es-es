---
title: Atributos de función
description: Los atributos \ callback\ y \ local\ se pueden aplicar como atributos de función.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be36cac561a10ae2e1177c29dfc0e1219f650daf26af8154c47cdbd7e3d2bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021027"
---
# <a name="function-attributes"></a>Atributos de función

La **\[** [**devolución de**](/windows/desktop/Midl/callback) **\]** llamada y los atributos **\[** [**locales**](/windows/desktop/Midl/local) se pueden aplicar como **\]** atributos de función.

Una devolución de llamada es una llamada remota desde el servidor al cliente que se ejecuta como parte de un subproceso conceptual de ejecución única. Una devolución de llamada siempre se emite en el contexto de una llamada remota (o devolución de llamada) y la ejecuta el subproceso que emitió la llamada remota original (o devolución de llamada).

A menudo es conveniente colocar una declaración de procedimiento local en el archivo IDL, ya que este es el lugar lógico para describir las interfaces de un paquete. El **\[** [**atributo local**](/windows/desktop/Midl/local) **\]** indica que una declaración de procedimiento no es realmente una función remota, sino un procedimiento local. El compilador MIDL no genera ningún código auxiliar para las funciones con el **\[ atributo local. \]**

Es importante tener en cuenta que no se recomienda el uso de la **\[** [**devolución**](/windows/desktop/Midl/callback) de **\]** llamada en la programación multiproceso. Como función de programación de un solo subproceso, no está equipado para admitir las demandas de seguridad que proporciona un entorno de varios subprocesos.

 

 