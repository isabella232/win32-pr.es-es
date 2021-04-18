---
description: ELS admite las funciones definidas en la tabla siguiente.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funciones de servicios lingüísticos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652795"
---
# <a name="extended-linguistic-services-functions"></a>Funciones de servicios lingüísticos extendidos

ELS admite las funciones definidas en la tabla siguiente.



| Función                                                 | Descripción                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Función de devolución de llamada definida por la aplicación que procesa asincrónicamente los datos generados por la función **MappingRecognizeText** .                 |
| [**MappingDoAction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Hace que un servicio ELS realice una acción después de que se haya producido el reconocimiento del texto.                                                                |
| [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Libera memoria y recursos asignados durante una operación de reconocimiento de texto de ELS.                                                                 |
| [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Libera la memoria y los recursos asignados para que la aplicación interactúe con uno o más servicios de ELS.                                            |
| [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Recupera una lista de los servicios compatibles con la plataforma ELS disponibles, junto con la información asociada, según los criterios especificados por la aplicación. |
| [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Llama a un servicio ELS para reconocer texto.                                                                                                   |



 

 

 



