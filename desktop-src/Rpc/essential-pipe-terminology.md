---
title: Terminología de canalización esencial
description: Al igual que otros tipos de parámetros a llamadas a procedimientos remotos, las canalizaciones pueden ser \ in \ o \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533405"
---
# <a name="essential-pipe-terminology"></a>Terminología de canalización esencial

Al igual que otros tipos de parámetros a llamadas a procedimientos remotos, las canalizaciones pueden ser \[ [**in**](/windows/desktop/Midl/in) \] o \[ [**out**](/windows/desktop/Midl/out-idl) \] . Puesto que el servidor controla la transferencia de datos a través de una canalización, se dice que las canalizaciones con el \[  \] atributo in *extraen* datos al servidor. Del mismo modo, las canalizaciones de salida *envían* datos del servidor al cliente. Los procedimientos que realizan la transferencia de datos se denominan *procedimiento de extracción* y el *procedimiento de inserción*, respectivamente.

El compilador MIDL genera los procedimientos de inserción y extracción para el servidor. Además, administra la asignación de búferes de datos en la memoria. Sin embargo, el cliente debe proporcionar sus propios procedimientos de inserción y extracción. También debe proporcionar un procedimiento para asignar los búferes de memoria utilizados por la canalización. El código auxiliar del cliente llama a estos automáticamente en el momento adecuado. El procedimiento de asignación se denomina a menudo procedimiento de asignación o la función de asignación.

 

 