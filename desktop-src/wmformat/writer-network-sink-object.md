---
title: Objeto de receptor de red writer
description: Objeto de receptor de red writer
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows SDK de formato multimedia, objetos receptores de red writer
- Formato de sistemas avanzados (ASF), objetos receptores de red de escritura
- ASF (formato de sistemas avanzados), escritura de objetos receptores de red
- objects,writer network sink objects
- objetos receptores de red writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2011fd161fc4ac5e1cd03d955f06259e6499e343970cc309b1e8c41db051a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843730"
---
# <a name="writer-network-sink-object"></a>Objeto de receptor de red writer

El objeto de receptor de red de escritor se usa para escribir medios digitales en una red.

La función [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)crea el objeto de receptor de red del escritor, que establece un puntero a una **interfaz IWMWriterNetworkSink.** Las demás interfaces del objeto de receptor de red del escritor se pueden obtener llamando al **método QueryInterface.**



| Interfaz                                              | Descripción                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Recopila información sobre los clientes conectados.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera información avanzada del cliente.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Permite que la aplicación obtenga mensajes de estado del objeto .                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Abre y cierra puertos, establece y recupera el número máximo de clientes que pueden conectarse al objeto receptor, establece el protocolo de red que usará el objeto de escritor y realiza otras funciones avanzadas. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Asigna memoria, determina si el receptor funciona en tiempo real y controla varias funciones de devolución de llamada.                                                                                                |



 

La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar un seguimiento del progreso de un objeto receptor de red de escritor.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Se requiere cuando se debe comunicar la información de estado a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Difusión de datos de ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




