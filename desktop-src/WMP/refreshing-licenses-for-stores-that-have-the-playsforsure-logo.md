---
title: Actualizar licencias para tiendas que tienen el logotipo PlaysForSure
description: Actualizar licencias para tiendas que tienen el logotipo PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Reproductor de Windows Media en línea, actualizar licencias
- tiendas en línea, actualización de licencias
- Reproductor de Windows Media en línea, actualización de licencias
- tiendas en línea, actualizar licencias
- Reproductor de Windows Media online stores,PlaysForSure logo
- tiendas en línea, logotipo de PlaysForSure
- actualizar licencias
- licenses,refreshing
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568213"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Actualizar licencias para tiendas que tienen el logotipo PlaysForSure

Algunas tiendas de música en línea tienen el logotipo PlaysForSure, pero no están integradas con Reproductor de Windows Media 11. Esos almacenes deben proporcionar un documento ServiceInfo y un componente ligero para que Reproductor de Windows Media 11 pueda obtener y actualizar licencias para su contenido.

En el ejemplo siguiente se muestra cómo funciona el proceso de actualización de licencias.

1.  El usuario obtiene 50 pistas de música de la tienda en línea Proseware. Cada pista es un archivo con la extensión de nombre de archivo .wma. Junto con las pistas, el usuario obtiene licencias para reproducir las pistas.
2.  El usuario copia las 50 pistas en un nuevo equipo que tiene Reproductor de Windows Media 11 instalado y agrega las pistas a la biblioteca Reproductor de Windows Media.
3.  En algún momento posterior, el Módulo de actualización de licencias (LRM), que forma parte de Reproductor de Windows Media 11, inspecciona los metadatos en las pistas de cincuenta y determina que Proseware es el proveedor de contenido.
    > [!Note]  
    > Reproductor de Windows Media puede identificar el proveedor de contenido inspeccionando el atributo **ContentDistributor** en un archivo multimedia. Si una tienda en línea que tiene el logotipo PlaysForSure proporciona un archivo multimedia que usa Windows Media Digital Rights Management (WMDRM), la tienda en línea debe colocar el atributo **ContentDistributor** en el archivo multimedia. Para obtener más información, vea Adding the Content Distributor Attribute in the Reproductor de Windows Media SDK (Agregar el atributo del distribuidor de contenido en el SDK de Reproductor de Windows Media contenido).

     

4.  El LRM busca la dirección URL del documento ServiceInfo de Proseware, descarga el documento e inspecciona el elemento **Install** del documento para obtener la dirección URL de un paquete que el LRM puede usar para instalar el componente de Proseware. El LRM instala y carga el componente.
5.  Para cada una de las 50 pistas, el LRM llama al método [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del componente Proseware. El **método allowPlay** coloca una licencia para la pista individual en el nuevo equipo y devuelve **TRUE en** el parámetro *pfAllowPlay.*
    > [!Note]  
    > El componente Proseware debe proporcionar todas las licencias necesarias para reproducir la pista individual. Es decir, el componente debe proporcionar una licencia raíz y una licencia hoja si es necesario.

     

    Durante la primera llamada al método **allowPlay,** el componente Proseware debe mostrar un cuadro de diálogo para comprobar que el usuario actual tiene una cuenta de Proseware y tiene derecho a reproducir la pista. Durante las llamadas posteriores a **allowPlay**, el componente puede usar las credenciales que obtuvo en la primera llamada para comprobar que el usuario tiene derecho a reproducir las pistas restantes.

El componente, escrito por el almacén en línea, debe implementar el **método allowPlay** de la **interfaz IWMPSubscriptionService.** El componente debe devolver E NOTIMPL de cada uno de los otros tres \_ métodos: **allowCDTransfer,** **allowPDATransfer** y **startBackgroundProcessing.** Además, el componente debe establecer el valor de la entrada del Registro **Capabilities** en 1; Es decir, se debe establecer la marca de funcionalidad SUBSCRIPTION CAP ALLOWPLAY y todas las demás marcas de \_ \_ funcionalidad deben borrarse. Para obtener más información sobre cómo registrar el componente, vea Claves y entradas del Registro [para un almacén en línea de tipo 2.](registry-keys-and-entries-for-a-type-2-online-store.md)

Para obtener información sobre cómo crear un componente que implementa la interfaz **IWMPSubscriptionService,** vea [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).

Para obtener información sobre cómo proporcionar a Microsoft un documento ServiceInfo, envíe un correo electrónico al equipo Reproductor de Windows Media Virtual Services. La dirección de correo electrónico del equipo es mpsvctm@microsoft.com .

Para obtener instrucciones técnicas sobre el uso de diversos SDK de Windows Media para crear un servicio que ofrece contenido multimedia digital con licencia, vaya al Centro para desarrolladores de [Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) y busque "Creación de una tienda en línea de suscripción de Reproductor de Windows Media 10".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Reproductor de Windows Media Tiendas en línea**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




