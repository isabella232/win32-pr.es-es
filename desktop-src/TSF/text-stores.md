---
title: Almacenes de texto
description: Almacenes de texto
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Services Framework (TSF), almacenes de texto
- TSF (marco de trabajo de servicios de texto), almacenes de texto
- Aplicaciones habilitadas para TSF, almacenes de texto
- almacenes de texto
- Marco de trabajo de servicios de texto (TSF), posición de caracteres de aplicación (ACP)
- TSF (marco de trabajo de servicios de texto), posición de carácter de aplicación (ACP)
- Aplicaciones habilitadas para TSF, posición de caracteres de aplicación (ACP)
- Posición de carácter de aplicación (ACP)
- ACP (posición de carácter de aplicación)
- Text Services Framework (TSF), delimitadores
- TSF (marco de trabajo de servicios de texto), delimitadores
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
- Marco de trabajo de servicios de texto (TSF), bloqueos de documento
- TSF (marco de trabajo de servicios de texto), bloqueos de documento
- Aplicaciones habilitadas para TSF, bloqueos de documentos
- bloqueos de documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077942"
---
# <a name="text-stores"></a>Almacenes de texto

## <a name="application-character-position-acp"></a>Posición de carácter de aplicación (ACP)

Un ACP es la ubicación de un carácter o caracteres en una secuencia de texto que se expresa como el número de caracteres desde el inicio de la secuencia de texto. Dado que el modelo ACP es de base cero, el primer carácter de una secuencia de texto tiene un ACP de cero. Por ejemplo:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Un almacén de texto implementa un objeto que admite la interfaz [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , lo que permite expresar el flujo de texto en un ACP. Los métodos de interfaz **ITextStoreACP** usan el intervalo ACP de la secuencia de texto para modificar el texto.

## <a name="anchor-based-applications"></a>Aplicaciones Anchor-Based

El administrador usa los métodos basados en ACP de forma nativa para manipular el texto. Sin embargo, un enfoque basado en anclaje está disponible para los clientes de [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) que admiten [delimitadores](ranges.md), por lo que el administrador usa los métodos [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) y [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) para encapsular los métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) y [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .

## <a name="document-access-control"></a>Access Control de documento

El almacén de texto controla el acceso a la secuencia de texto mediante [bloqueos de documento](document-locks.md). Para leer o modificar el almacén de texto, el administrador debe instalar primero un receptor de notificaciones que admita la interfaz [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) llamando al método [ITextStoreACP:: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) y pasando un puntero a un receptor de notificaciones. El receptor de notificaciones permite al administrador obtener un bloqueo de documento en el almacén de texto y recibir notificaciones cuando el almacén de texto se modifica con otro elemento que no sea el administrador, como la entrada del usuario a través de la aplicación. Los receptores de notificaciones se tratan más adelante en este tema.

## <a name="how-to-initialize-the-text-store"></a>Cómo inicializar el almacén de texto

Una aplicación Inicializa un almacén de texto completando los pasos siguientes:

1.  Cree un objeto de administrador de subprocesos basado en la interfaz [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) llamando a la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un puntero a un objeto de administrador de subprocesos. El siguiente es un ejemplo de código de la implementación de un objeto de administrador de subprocesos.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Active el objeto de administrador de subprocesos llamando al método [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) . Este método proporciona un puntero a un [identificador de cliente](tfclientid.md) que se usa para crear un objeto de contexto. El administrador de subprocesos se usa para implementar un objeto de administrador de documentos.
3.  Cree un objeto de administrador de documentos basado en la interfaz [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) llamando al método [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) con un puntero al objeto de administrador de documentos. El objeto de administrador de documentos se usa para implementar un objeto de contexto que es el almacén de texto.
4.  Cree un objeto de contexto desde el administrador de documentos mediante una llamada al método [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) con el puntero al objeto de almacén de texto y un puntero al identificador de cliente para activar el administrador de subprocesos. El siguiente es un ejemplo de cómo crear un objeto de contexto:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Inserte el objeto de contexto en la pila con el método [ITfDocumentMgr::P uscripción](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) . El siguiente es un ejemplo de cómo insertar el objeto de contexto en la pila:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Cómo modificar el almacén de texto

El método **ITfDocumentMgr::P uscripción** llama a **ITextStoreACP:: AdviseSink** con un puntero a la interfaz del receptor de notificaciones para instalar un nuevo receptor de notificaciones o modificar un receptor de notificaciones existente. El receptor de notificaciones recibe notificaciones cuando el almacén de texto se modifica con otro elemento que no sea el administrador, como la entrada del usuario en la aplicación. Las aplicaciones deben llamar al método [ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) cuando el método de entrada obtiene el foco. Otras notificaciones del administrador de subprocesos se proporcionan mediante una llamada a los métodos de interfaz **ITextStoreACPSink** adecuados.

Sin embargo, las aplicaciones no deben llamar a los métodos de la interfaz **ITextStoreACPSink** en respuesta a los métodos de interfaz **ITextStoreACP** . Las aplicaciones solo deben llamar a los métodos de la interfaz **ITextStoreACPSink** cuando el almacén de texto se modifique con otro elemento que no sea el administrador.

El contenido del almacén de texto se puede modificar con un estado de entrada temporal denominado [composición](compositions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delimitadores](ranges.md)
</dt> <dt>

[Composiciones](compositions.md)
</dt> <dt>

[Bloqueos de documento](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 