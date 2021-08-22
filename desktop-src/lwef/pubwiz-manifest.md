---
title: Uso del manifiesto de transferencia
description: El Asistente para publicación web y el Asistente para ordenación de impresión en línea usan el manifiesto de transferencia para comunicar los detalles de la transferencia de datos entre el equipo cliente y el sitio del servidor.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Asistente para publicación web, manifiesto de transferencia
- Asistente para pedidos de impresión en línea, manifiesto de transferencia
- manifiesto de transferencia
- manifest
- window.external,transfer manifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d7f4ea3f9cd392f4b0bab50e1e558613fc7485d4f44a27472cd48ad898b3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555855"
---
# <a name="using-the-transfer-manifest"></a>Uso del manifiesto de transferencia

El Asistente para publicación web y el Asistente para ordenación de impresión en línea usan el manifiesto de transferencia para comunicar los detalles de la transferencia de datos entre el equipo cliente y el sitio del servidor.

## <a name="the-purpose-of-the-transfer-manifest"></a>El propósito del manifiesto de transferencia

El manifiesto de transferencia describe los archivos implicados en la transferencia, incluidos detalles como la jerarquía de destino y los metadatos del archivo. El script del lado servidor puede modificar el manifiesto quitando archivos inadecuados de la lista y agregando información sobre cómo y dónde se deben transferir los archivos.

El manifiesto se expone como la propiedad **window.external.Property("TransferManifest")**, un documento xml Document Object Model (DOM). Para obtener más información sobre EL DOM XML, vea la documentación de MSDN para [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

La organización de nivel superior del manifiesto de transferencia es la siguiente:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



La página HTML del lado servidor puede usar los nodos del manifiesto para obtener cierta información sobre los archivos que se van a copiar y, a continuación, modificar la interfaz de usuario del servicio en consecuencia. Por ejemplo, un sitio de impresión de fotos podría usar la información para mostrar miniaturas de las imágenes elegidas, mientras que un sitio de almacenamiento podría usar la información para asegurarse de que hay suficiente espacio de almacenamiento disponible para ese usuario. Para obtener información completa sobre los nodos y atributos del manifiesto de transferencia, vea [Transferir esquema de manifiesto.](/windows/desktop/shell/interfaces)

El esquema del manifiesto de transferencia se escribe como un modelo abierto para que los elementos no definidos específicamente en el esquema puedan aparecer en el manifiesto de transferencia. Por lo tanto, un sitio de proveedor podría agregar elementos propietarios para su propio uso sin alterar la validez del manifiesto. El esquema también se define para que el orden de los elementos no esté restringido.

> [!Note]  
> El manifiesto se vuelve a crear cada vez que se elige un nuevo proveedor para que tenga la oportunidad de almacenar información del sitio en el manifiesto.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de manifiesto de transferencia](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 