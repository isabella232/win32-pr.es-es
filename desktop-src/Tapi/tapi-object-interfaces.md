---
description: El objeto TAPI es el objeto principal de TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces de objetos TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1e49fe83a75c802b06ded953f309a157365d482d22d06c6bbedf97a5b8ac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139858"
---
# <a name="tapi-object-interfaces"></a>Interfaces de objetos TAPI

El [objeto TAPI](tapi-object.md) es el objeto principal de TAPI 3.

La [**interfaz ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) no se expone directamente en el objeto TAPI, pero está estrechamente relacionada con él y se muestra aquí para mayor comodidad de referencia.



| Interfaces                                                 | Descripción                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Interfaz TAPI 3 principal.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Deriva de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); proporciona métodos adicionales que admiten dispositivos de teléfono.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Interfaz saliente que se usa para recibir información asincrónica sobre los eventos TAPI 3.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Proporciona una interfaz de entrada en los controles del centro de llamadas.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Proporciona métodos para recuperar información relacionada con los eventos de objeto TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Extiende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); proporciona un método para recuperar un puntero al objeto de teléfono que produjo el evento de objeto TAPI. |



 

 

 
