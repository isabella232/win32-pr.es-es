---
title: Almacenes de texto
description: Almacenes de texto
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Services Framework (TSF),almacenes de texto
- TSF (Text Services Framework),almacenes de texto
- Aplicaciones habilitadas para TSF, almacenes de texto
- almacenes de texto
- Text Services Framework (TSF),Posición de caracteres de aplicación (ACP)
- TSF (Text Services Framework),Posición de caracteres de aplicación (ACP)
- Aplicaciones habilitadas para TSF, posición de caracteres de aplicación (ACP)
- Posición de caracteres de aplicación (ACP)
- ACP (posición del carácter de aplicación)
- Text Services Framework (TSF),anchors
- TSF (Text Services Framework),anchors
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
- Text Services Framework (TSF), bloqueos de documentos
- TSF (Text Services Framework), bloqueos de documentos
- Aplicaciones habilitadas para TSF, bloqueos de documentos
- bloqueos de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068807"
---
# <a name="text-stores"></a>Almacenes de texto

## <a name="application-character-position-acp"></a>Posición de caracteres de aplicación (ACP)

Un ACP es la ubicación de un carácter, o caracteres, en una secuencia de texto que se expresa como el número de caracteres desde el principio de la secuencia de texto. Dado que el modelo ACP está basado en cero, el primer carácter de una secuencia de texto tiene un ACP de cero. Por ejemplo:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Un almacén de texto implementa un objeto que admite la interfaz [ITextStoreACP,](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) que permite expresar la secuencia de texto en una ACP. Los **métodos de interfaz ITextStoreACP** usan el intervalo ACP de la secuencia de texto para modificar el texto.

## <a name="anchor-based-applications"></a>Anchor-Based aplicaciones

El administrador usa los métodos basados en ACP de forma nativa para manipular texto. Sin embargo, hay disponible un enfoque basado en delimitadores para los clientes de [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) que admiten delimitadores, por lo que el administrador usa los [métodos](ranges.md) [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) para encapsular los métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink.](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)

## <a name="document-access-control"></a>Documento Access Control

El almacén de texto controla el acceso a la secuencia de texto mediante [bloqueos de documento.](document-locks.md) Para leer o modificar el almacén de texto, el administrador debe instalar primero un receptor de asesoramiento que admita la interfaz [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) llamando al método [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) y pasando un puntero a un receptor de asesoramiento. El receptor de asesoramiento permite al administrador obtener bloqueos de documento en el almacén de texto y recibir notificaciones cuando el almacén de texto se modifica por otro que no sea el administrador, como la entrada del usuario a través de la aplicación. Los receptores de asesoramiento se deban tratar más adelante en este tema.

## <a name="how-to-initialize-the-text-store"></a>Cómo inicializar el almacén de texto

Una aplicación inicializa un almacén de texto completando los pasos siguientes:

1.  Cree un objeto de administrador de subprocesos basado en la [interfaz ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) llamando a la [función CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un puntero a un objeto de administrador de subprocesos. A continuación se muestra un ejemplo de código de implementación de un objeto de administrador de subprocesos.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Active el objeto del administrador de subprocesos llamando al [método ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) Este método proporciona un puntero a un identificador [de cliente utilizado](tfclientid.md) para crear un objeto de contexto. El administrador de subprocesos se usa para implementar un objeto de administrador de documentos.
3.  Cree un objeto de administrador de documentos basado en la interfaz [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) mediante una llamada al método [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) con un puntero al objeto del administrador de documentos. El objeto del administrador de documentos se usa para implementar un objeto de contexto que es el almacén de texto.
4.  Cree un objeto de contexto desde el administrador de documentos llamando al método [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) con el puntero al objeto de almacén de texto y un puntero al identificador de cliente al activar el administrador de subprocesos. A continuación se muestra un ejemplo de creación de un objeto de contexto:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Inserta el objeto de contexto en la pila con [el método ITfDocumentMgr::P ush.](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) A continuación se muestra un ejemplo de cómo insertar el objeto de contexto en la pila:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Cómo modificar el almacén de texto

El **método ITfDocumentMgr::P ush** llama a **ITextStoreACP::AdviseSink** con un puntero a la interfaz del receptor de asesoramiento para instalar un nuevo receptor de asesoramiento o modificar un receptor de asesoramiento existente. El receptor de notificaciones recibe notificaciones cuando el almacén de texto se modifica por otro que no sea el administrador, como la entrada del usuario a la aplicación. Las aplicaciones deben llamar [al método ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) cuando el método de entrada obtiene el foco. Se proporcionan otras notificaciones al administrador de subprocesos mediante una llamada a los métodos de interfaz **ITextStoreACPSink** adecuados.

Sin embargo, las aplicaciones no deben llamar a los métodos de interfaz **ITextStoreACPSink** en respuesta a los métodos **de interfaz ITextStoreACP.** Las aplicaciones solo deben llamar a los métodos de interfaz **ITextStoreACPSink** cuando el almacén de texto se modifica por otro que no sea el administrador.

El contenido del almacén de texto se puede modificar con un estado de entrada temporal denominado [composición](compositions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delimitadores](ranges.md)
</dt> <dt>

[Composiciones](compositions.md)
</dt> <dt>

[Bloqueos de documentos](document-locks.md)
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

 

 