---
title: Objeto de receptor de red del escritor
description: Objeto de receptor de red del escritor
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- SDK de Windows Media Format, objetos de receptor de red del escritor
- Advanced Systems Format (ASF), objetos de receptor de red del escritor
- ASF (formato de sistemas avanzados), objetos de receptor de red del sistema de escritura
- objetos, objetos de receptor de red del escritor
- objetos de receptor de red del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149129"
---
# <a name="writer-network-sink-object"></a>Objeto de receptor de red del escritor

El objeto de receptor de red del escritor se utiliza para escribir medios digitales en una red.

La función [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)crea el objeto de receptor de red del escritor, que establece un puntero a una interfaz **IWMWriterNetworkSink** . Las demás interfaces del objeto de receptor de red del escritor se pueden obtener llamando al método **QueryInterface** .



| Interfaz                                              | Descripción                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Recopila información sobre los clientes conectados.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Recupera información de cliente avanzada.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Permite que la aplicación obtenga mensajes de estado del objeto.                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Abre y cierra los puertos, establece y recupera el número máximo de clientes que pueden conectarse al objeto de receptor, establece el protocolo de red que va a usar el objeto de escritor y realiza otras funciones avanzadas. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Asigna memoria, determina si el receptor está funcionando en tiempo real y controla varias funciones de devolución de llamada.                                                                                                |



 

La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de un objeto de receptor de red del escritor.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obligatorio cuando la información de estado se debe comunicar a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Difusión de datos de ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




