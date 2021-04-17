---
description: El objeto TAPI es el objeto principal de TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces de objeto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678233"
---
# <a name="tapi-object-interfaces"></a>Interfaces de objeto TAPI

El [objeto TAPI](tapi-object.md) es el objeto principal de TAPI 3.

La interfaz [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) no se expone directamente en el objeto TAPI, pero está estrechamente relacionada con ella y se muestra aquí para mayor comodidad de referencia.



| Interfaces                                                 | Descripción                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Interfaz TAPI 3 principal.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Deriva de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); proporciona métodos adicionales que admiten dispositivos telefónicos.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Interfaz de salida que se usa para recibir información asincrónica acerca de los eventos TAPI 3.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Proporciona una interfaz de entrada en los controles del centro de llamadas.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Proporciona métodos para recuperar información relacionada con eventos de objetos TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Extiende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); proporciona un método para recuperar un puntero al objeto de teléfono que causó el evento de objeto TAPI. |



 

 

 
