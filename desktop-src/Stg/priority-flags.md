---
title: Marcas de prioridad
description: La marca de prioridad abre un objeto de almacenamiento en modo de prioridad.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Marcas de prioridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076405"
---
# <a name="priority-flags"></a>Marcas de prioridad

La marca de prioridad abre un objeto de almacenamiento en modo de prioridad. Cuando abre un objeto, una aplicación suele trabajar desde una copia de la instantánea, ya que otras aplicaciones también pueden utilizar el objeto al mismo tiempo. Sin embargo, al abrir un objeto de almacenamiento en modo de prioridad, la aplicación tiene derechos exclusivos para confirmar cambios en el objeto.

El modo de prioridad permite que una aplicación Lea algunas secuencias del almacenamiento antes de abrir el objeto en un modo que requeriría que el sistema realizara una copia de la instantánea. Dado que la aplicación tiene acceso exclusivo, no tiene que realizar una copia de instantánea del objeto. Cuando la aplicación abre posteriormente el objeto en un modo en el que se requiere una copia de instantánea, la aplicación puede excluir los flujos que ya ha leído de la instantánea, lo que reduce la sobrecarga de abrir el objeto.

Dado que otras aplicaciones no pueden confirmar los cambios en un objeto mientras está abierto en modo de prioridad, las aplicaciones deben mantener el objeto en ese modo lo más corto posible.

 

 




