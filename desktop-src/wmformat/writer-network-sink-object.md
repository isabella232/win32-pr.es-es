---
title: Objeto receptor de red writer
description: Objeto receptor de red writer
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows SDK de formato multimedia, objetos receptores de red de escritor
- Formato de sistemas avanzados (ASF), objetos receptores de red de escritura
- ASF (formato de sistemas avanzados), objetos receptores de red de escritura
- objects,writer network sink objects
- objetos receptores de red writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359553"
---
# <a name="writer-network-sink-object"></a>Objeto receptor de red writer

El objeto receptor de red de escritor se usa para escribir medios digitales en una red.

El objeto receptor de red writer se crea mediante la función [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), que establece un puntero a una **interfaz IWMWriterNetworkSink.** Las demás interfaces del objeto receptor de red del escritor se pueden obtener llamando al **método QueryInterface.**



| Interfaz                                              | Descripción                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Recopila información sobre los clientes conectados.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera información avanzada del cliente.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Permite que la aplicación obtenga mensajes de estado del objeto .                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Abre y cierra puertos, establece y recupera el número máximo de clientes que se pueden conectar al objeto receptor, establece el protocolo de red que va a usar el objeto de escritor y realiza otras funciones avanzadas. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Asigna memoria, determina si el receptor funciona en tiempo real y controla varias funciones de devolución de llamada.                                                                                                |



 

La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar un seguimiento del progreso de un objeto receptor de red de escritor.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Se requiere cuando la información de estado se debe comunicar a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Difusión de datos de ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




