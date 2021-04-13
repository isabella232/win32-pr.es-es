---
title: Composiciones
description: Una composición es un estado de entrada temporal que permite a un servicio de texto especificar tanto a la aplicación como al usuario que el texto de entrada sigue en un estado de cambio.
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- Text Services Framework (TSF), composiciones
- TSF (marco de trabajo de servicios de texto), composiciones
- servicios de texto, composiciones
- Aplicaciones habilitadas para TSF, composiciones
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b03f3e991f76ee7c6dca3830267796576c7b842
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421188"
---
# <a name="compositions"></a>Composiciones

Una composición es un estado de entrada temporal que permite a un servicio de texto especificar tanto a la aplicación como al usuario que el texto de entrada sigue en un estado de cambio. Una aplicación puede y debe obtener información sobre el atributo de presentación sobre la composición y utilizar esta información para mostrar el estado de composición al usuario.

Un ejemplo del uso de una composición es durante la entrada de voz. Mientras el usuario está hablando, el servicio de texto de voz crea una composición. Esta composición permanecerá intacta hasta que se complete toda la entrada de voz. Cuando finaliza la sesión, el servicio de texto de voz finaliza la composición.

Una aplicación utiliza la presencia y la ausencia de una composición para determinar cómo mostrar texto y qué procesamiento se debe realizar en el texto. Por ejemplo, si el usuario usa el motor de voz para introducir texto, la aplicación no debe realizar ninguna revisión ortográfica o gramatical en ningún texto de la composición. El texto se considera incompleto hasta que se termina la composición.

## <a name="text-services"></a>Servicios de texto

Un servicio de texto crea una composición mediante una llamada a [ITfContextComposition:: StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition). El servicio de texto puede implementar opcionalmente un objeto [ITfCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) que recibe notificaciones de eventos de composición. StartComposition devuelve un objeto [ITfComposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) al que el servicio de texto mantiene una referencia y utiliza para modificar y finalizar la composición. El servicio de texto finaliza la composición mediante una llamada a [ITfComposition:: EndComposition](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition).

Si un servicio de texto va a crear composiciones, también debe admitir atributos de presentación para permitir que una aplicación muestre texto que forma parte de una composición de forma distinta que el texto estándar. Para obtener más información, vea [proporcionar atributos para mostrar](providing-display-attributes.md).

## <a name="applications"></a>APLICACIONES

Una aplicación puede supervisar la creación, el cambio y la finalización de las composiciones mediante la instalación de un receptor de [ITfContextOwnerCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) . Cuando se inicia una composición, se llama a [ITfContextOwnerCompositionSink:: OnStartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) . Del mismo modo, cuando se cambia o finaliza una composición, se llamará a [ITfContextOwnerCompositionSink:: OnUpdateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) y [ITfContextOwnerCompositionSink:: OnEndComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) , respectivamente.

El siguiente es un procedimiento típico para actualizar un documento mediante una composición.

1.  [ITextStoreACP:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) o [ITextStoreAnchor:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) se usan normalmente para insertar el texto inicial en la composición.
2.  La composición se inicia con una llamada a [ITfContextComposition:: StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition), utilizando el intervalo de texto devuelto por **InsertTextAtSelection**.
3.  Cuando recibe una entrada nueva, como la entrada de voz o el teclado, la aplicación actualiza la composición con [ITextStoreACP:: setText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) o [ITextStoreAnchor:: setText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext).
4.  Cuando la aplicación determina que es el momento de finalizar la composición, llama a [ITfComposition:: EndComposition](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition).

La aplicación debe usar los atributos de presentación proporcionados por el servicio de texto para modificar la presentación de texto en todo momento y no solo cuando una composición está activa. Para obtener más información, vea [using display Attributes](using-display-attributes.md).

Si es necesario, una aplicación puede finalizar una composición mediante una llamada a [ITfContextOwnerCompositionServices:: TerminateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition).

 

 