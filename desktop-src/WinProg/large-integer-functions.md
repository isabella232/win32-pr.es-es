---
title: Funciones de enteros grandes
description: Las siguientes funciones se usan con enteros grandes.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aebb5bd8c3edc35098dcf1bb232d858a9c6638d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075865"
---
# <a name="large-integer-functions"></a>Funciones de enteros grandes

Las siguientes funciones se usan con enteros grandes.

## <a name="in-this-section"></a>En esta sección



| Función                                                                    | Descripción                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Multiplica dos enteros de 32 bits con signo y devuelve un resultado entero de 64 bits con signo.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Realiza una operación de desplazamiento lógico a la izquierda en un valor entero de 64 bits sin signo. La función proporciona un código de desplazamiento mejorado para los turnos lógicos de la izquierda en los que el número de turnos está en el intervalo de 0-31.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Realiza una operación de desplazamiento aritmético a la derecha en un valor entero de 64 bits con signo. La función proporciona un código de desplazamiento mejorado para los turnos aritméticos correctos en los que el número de turnos está en el intervalo de 0-31.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Realiza una operación de desplazamiento lógico a la derecha en un valor entero de 64 bits sin signo. La función proporciona un código de desplazamiento mejorado para los turnos lógicos correctos en los que el número de turnos está en el intervalo 0-31.<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Multiplica valores de 2 32 bits y, a continuación, divide el resultado de 64 bits por un tercer valor de 32 bits.<br/>                                                                                                           |
| [**Multiply128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Multiplica los enteros de 2 64 bits para generar un entero de 128 bits.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Multiplica los enteros de 2 64 bits para generar un entero de 128 bits, desplaza el producto a la derecha el número de bits especificado y devuelve los bits de 64 inferiores del resultado.<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Multiplica los enteros de 2 64 bits para generar un entero de 128 bits y obtiene los bits grandes de 64.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Cuenta el número de un bit (recuento de población) en un entero de 64 bits sin signo.<br/>                                                                                                                     |
| [**ShiftLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Desplaza a la izquierda 128 bits.<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Desplaza a la derecha 128 bits.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Multiplica dos enteros de 32 bits sin signo y devuelve un resultado entero de 64 bits sin signo.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Multiplica dos enteros de 64 bits sin signo para generar un entero de 128 bits sin signo.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Multiplica dos enteros de 64 bits sin signo para producir un entero de 128 bits sin signo, desplaza el producto a la derecha el número de bits especificado y devuelve los bits de 64 inferiores del resultado.<br/>        |
| [**UnsignedMulitplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Multiplica los enteros de 2 64 bits para generar un entero de 128 bits y obtiene los bits grandes sin signo de 64.<br/>                                                                                                    |



 

 

 





