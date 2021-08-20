---
title: Composiciones
description: Una composición es un estado de entrada temporal que permite a un servicio de texto especificar tanto a la aplicación como al usuario que el texto de entrada sigue en estado de cambio.
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- Text Services Framework (TSF), composiciones
- TSF (Text Services Framework),compositions
- servicios de texto, composiciones
- Aplicaciones habilitadas para TSF, composiciones
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a27d468c770e0593f61a5d57aeaedca15f241300da71dc7b617c74b8f1e7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953842"
---
# <a name="compositions"></a>Composiciones

Una composición es un estado de entrada temporal que permite a un servicio de texto especificar tanto a la aplicación como al usuario que el texto de entrada sigue en estado de cambio. Una aplicación puede y debe obtener información de atributos para mostrar sobre la composición y usar esta información para mostrar el estado de composición al usuario.

Un ejemplo del uso de una composición es durante la entrada de voz. Mientras el usuario habla, el servicio de texto de voz crea una composición. Esta composición permanecerá intacta hasta que se complete toda la entrada de voz. Cuando finaliza la sesión, el servicio de texto de voz finaliza la composición.

Una aplicación usa la presencia y ausencia de una composición para determinar cómo mostrar texto y qué procesamiento, si existe, se debe realizar en el texto. Por ejemplo, si el usuario usa el motor de voz para escribir texto, la aplicación no debe realizar ninguna revisión ortográfica o gramatical en ningún texto de composición. El texto se considera incompleto hasta que finaliza la composición.

## <a name="text-services"></a>Servicios de texto

Un servicio de texto crea una composición mediante una [llamada a ITfContextComposition::StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition). Opcionalmente, el servicio de texto puede implementar un [objeto ITfCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) que recibe notificaciones de eventos de composición. StartComposition devuelve un [objeto ITfComposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) al que el servicio de texto mantiene una referencia y usa para modificar y finalizar la composición. El servicio de texto finaliza la composición llamando a [ITfComposition::EndComposition](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition).

Si un servicio de texto va a crear composiciones, también debe admitir atributos de presentación para permitir que una aplicación muestre texto que forma parte de una composición de forma diferente que el texto estándar. Para obtener más información, vea [Proporcionar atributos para mostrar.](providing-display-attributes.md)

## <a name="applications"></a>Aplicaciones

Una aplicación puede supervisar la creación, el cambio y la terminación de las composiciones mediante la instalación de un receptor [ITfContextOwnerCompositionSink.](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) Cuando se inicia una composición, [se llama a ITfContextOwnerCompositionSink::OnStartComposition.](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) Del mismo modo, cuando se cambia o finaliza una composición, se llama a [ITfContextOwnerCompositionSink::OnUpdateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) e [ITfContextOwnerCompositionSink::OnEndComposition,](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) respectivamente.

A continuación se muestra un procedimiento típico para actualizar un documento mediante una composición.

1.  [ITextStoreACP::InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) o [ITextStoreAnchor::InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) se usan normalmente para insertar el texto inicial en la composición.
2.  La composición se inicia con una llamada a [ITfContextComposition::StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition), utilizando el intervalo de texto devuelto por **InsertTextAtSelection**.
3.  Cuando recibe una entrada nueva, como la entrada de voz o teclado, la aplicación actualiza la composición con [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) o [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext).
4.  Cuando la aplicación determina que es el momento de finalizar la composición, llama a [ITfComposition::EndComposition](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition).

La aplicación debe usar los atributos de presentación proporcionados por el servicio de texto para modificar la presentación de texto en todo momento y no solo cuando una composición está activa. Para obtener más información, vea [Usar atributos para mostrar.](using-display-attributes.md)

Si es necesario, una aplicación puede finalizar una composición llamando a [ITfContextOwnerCompositionServices::TerminateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition).

 

 