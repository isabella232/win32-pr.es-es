---
title: Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure
description: Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player tiendas en línea, actualizar licencias
- tiendas en línea, actualización de licencias
- Windows Media Player tiendas en línea, actualización de licencias
- tiendas en línea, actualizar licencias
- Windows Media Player tiendas en línea, logotipo de PlaysForSure
- tiendas en línea, logotipo de PlaysForSure
- actualizar licencias
- licencias, actualizar
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149098"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure

Algunos almacenes de música en línea tienen el logotipo de PlaysForSure, pero no se integran con Windows Media Player 11. Esos almacenes deben proporcionar un documento ServiceInfo y un componente ligero para que Windows Media Player 11 pueda obtener y actualizar las licencias de su contenido.

En el ejemplo siguiente se muestra cómo funciona el proceso de actualización de licencias.

1.  El usuario obtiene las pistas de música 50 de la tienda en línea de Proseware. Cada pista es un archivo con la extensión de nombre de archivo. WMA. Junto con las pistas, el usuario obtiene las licencias para reproducir las pistas.
2.  El usuario copia las pistas 50 en un nuevo equipo que tiene instalado Windows Media Player 11 y agrega las pistas a la biblioteca de Media Player de Windows.
3.  En algún momento posterior, el módulo de actualización de licencias (LRM), que forma parte de Windows Media Player 11, inspecciona los metadatos de las pistas 50 y determina que Proseware es el proveedor de contenido.
    > [!Note]  
    > Windows Media Player puede identificar el proveedor de contenido inspeccionando el atributo **ContentDistributor** en un archivo multimedia. Si una tienda en línea que tiene el logotipo de PlaysForSure proporciona un archivo multimedia que usa Windows Media Digital Rights Management (WMDRM), la tienda en línea debe colocar el atributo **ContentDistributor** en el archivo multimedia. Para obtener más información, vea Agregar el atributo distribuidor de contenido en el SDK de Windows Media Player.

     

4.  LRM busca la dirección URL del documento ServiceInfo de Proseware, descarga el documento e inspecciona el elemento **install** del documento para obtener la dirección URL de un paquete que LRM puede usar para instalar el componente de Proseware. LRM instala y carga el componente.
5.  Para cada una de las pistas 50, LRM llama al método [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del componente Proseware. El método **allowPlay** coloca una licencia para la pista individual en el nuevo equipo y devuelve **true** en el parámetro *pfAllowPlay* .
    > [!Note]  
    > El componente Proseware debe proporcionar todas las licencias necesarias para reproducir la pista individual. Es decir, el componente debe proporcionar una licencia raíz y una licencia de hoja, si es necesario.

     

    Durante la primera llamada al método **allowPlay** , el componente Proseware debe mostrar un cuadro de diálogo para comprobar que el usuario actual tiene una cuenta de Proseware y tiene derecho a reproducir la pista. Durante las llamadas posteriores a **allowPlay**, el componente puede usar las credenciales que obtuvo en la primera llamada para comprobar que el usuario tiene derecho a reproducir el resto de las pistas.

El componente, que está escrito por la tienda en línea, debe implementar el método **allowPlay** de la interfaz **IWMPSubscriptionService** . El componente debe devolver E \_ NOTIMPL de cada uno de los otros tres métodos: **allowCDBurn**, **allowPDATransfer** y **startBackgroundProcessing**. Además, el componente debe establecer el valor de la entrada del registro **Capabilities** en 1; es decir, se \_ debe establecer la marca de capacidad de límite de suscripción \_ ALLOWPLAY y se deben borrar todas las demás marcas de funcionalidad. Para obtener más información acerca del registro del componente, consulte [claves del registro y entradas para una tienda en línea de tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).

Para obtener información sobre cómo crear un componente que implemente la interfaz **IWMPSubscriptionService** , vea [crear el complemento para una tienda en línea de tipo 2](building-the-plug-in-for-a-type-2-online-store.md).

Para obtener información acerca de cómo proporcionar a Microsoft un documento ServiceInfo, envíe un correo electrónico al equipo de servicios virtuales de Windows Media Player. La dirección de correo electrónico del equipo es mpsvctm@microsoft.com .

Para obtener orientación técnica sobre el uso de una variedad de SDK de Windows Media para crear un servicio que ofrezca contenido multimedia digital con licencia, vaya al [Centro para desarrolladores de Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) y busque "crear una tienda en línea de suscripciones de Windows Media Player 10".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Windows Media Player tiendas en línea**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




