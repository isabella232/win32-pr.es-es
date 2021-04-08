---
title: Usar el manifiesto de transferencia
description: El Asistente para publicación web y el Asistente para la ordenación de impresión en línea utilizan el manifiesto de transferencia para comunicar detalles de la transferencia de datos entre el equipo cliente y el sitio del servidor.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Asistente para publicación Web, transferir manifiesto
- Asistente para orden de impresión en línea, transferir manifiesto
- transferir manifiesto
- manifest
- Window. external, transferir manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904595"
---
# <a name="using-the-transfer-manifest"></a>Usar el manifiesto de transferencia

El Asistente para publicación web y el Asistente para la ordenación de impresión en línea utilizan el manifiesto de transferencia para comunicar detalles de la transferencia de datos entre el equipo cliente y el sitio del servidor.

## <a name="the-purpose-of-the-transfer-manifest"></a>El propósito del manifiesto de transferencia

El manifiesto de transferencia describe los archivos implicados en la transferencia, incluidos los detalles como la jerarquía de destino y los metadatos del archivo. El script de servidor puede modificar el manifiesto quitando archivos inadecuados de la lista y agregando información sobre cómo y dónde se deben transferir los archivos.

El manifiesto se expone como la propiedad **window. external. Property ("TransferManifest")**, un documento de Document Object Model XML (dom). Para obtener más información acerca del DOM XML, vea la documentación de MSDN para [IXMLDOMDocument/DomDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

La organización de nivel superior del manifiesto de transferencia es la siguiente:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



La página HTML del lado servidor puede usar los nodos del manifiesto para obtener cierta información sobre los archivos que se van a copiar y, a continuación, modificar la interfaz de usuario del servicio en consecuencia. Por ejemplo, un sitio de impresión fotográfica podría usar la información para mostrar vistas en miniatura de las imágenes elegidas, mientras que un sitio de almacenamiento podría usar la información para asegurarse de que hay suficiente espacio de almacenamiento disponible para ese usuario. Para obtener información completa sobre los atributos y nodos del manifiesto de transferencia, vea [transferir el esquema del manifiesto](/windows/desktop/shell/interfaces).

El esquema de manifiesto de transferencia se escribe como un modelo abierto para que los elementos no definidos específicamente en el esquema puedan aparecer en el manifiesto de transferencia. Por lo tanto, un sitio de proveedor podría agregar elementos propietarios para su propio uso sin alterar la validez del manifiesto. También se define el esquema para que el orden de los elementos no esté restringido.

> [!Note]  
> El manifiesto se vuelve a crear cada vez que se elige un proveedor nuevo para que el proveedor tenga la oportunidad de almacenar información del sitio en el manifiesto.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferir esquema de manifiesto](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 