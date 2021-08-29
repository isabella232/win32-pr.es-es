---
description: ELS admite las funciones definidas en la tabla siguiente.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funciones extendidas de Linguistic Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c798a71e9973bce2e7f1bf8720c30877ab87019eeaff103a73b9b0fb7afd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041515"
---
# <a name="extended-linguistic-services-functions"></a>Funciones extendidas de Linguistic Services

ELS admite las funciones definidas en la tabla siguiente.



| Función                                                 | Descripción                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Función de devolución de llamada definida por la aplicación que procesa de forma asincrónica los datos generados por la **función MappingRecognizeText.**                 |
| [**MappingDoAction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Hace que un servicio ELS realice una acción después de que se haya producido el reconocimiento de texto.                                                                |
| [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Libera la memoria y los recursos asignados durante una operación de reconocimiento de texto de ELS.                                                                 |
| [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Libera la memoria y los recursos asignados para que la aplicación interactúe con uno o varios servicios de ELS.                                            |
| [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Recupera una lista de servicios compatibles con la plataforma elS disponibles, junto con la información asociada, según los criterios especificados por la aplicación. |
| [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Llama a un servicio ELS para reconocer texto.                                                                                                   |



 

 

 



