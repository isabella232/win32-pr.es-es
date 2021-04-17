---
description: Agregar nodos de transformación con TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Agregar nodos de transformación con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fa39457f8808070f93a4e5de31e181525ca33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360352"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Agregar nodos de transformación con TopoEdit

Un nodo de transformación representa una transformación de Media Foundation (MFT) que procesa los datos multimedia que recibe de un nodo de origen. Cuando está listo, la canalización lo pasa al nodo de salida para la representación. En Media Foundation, los codificadores, descodificadores, multiplexadores, demultiplexadores y efectos de vídeo de audio se implementan como MFTs. TopoEdit admite la adición de nodos de transformación que representan MFTs tanto registrados como personalizados.

Para obtener información sobre cómo agregar nodos de transformación mediante programación usando Media Foundation API, vea [crear nodos de transformación](creating-transform-nodes.md).

## <a name="to-add-a-registered-mft-to-the-topology"></a>Para agregar una MFT registrada a la topología

1.  En el menú **topología** , haga clic en **Agregar transformación**.

    Se abre el cuadro de diálogo **seleccionar transformación** . Muestra una lista clasificada de MFTs registrados que se genera mediante la enumeración de las entradas registradas en el registro mediante una llamada a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .

2.  Expanda la categoría y seleccione el MFT que desea agregar a la topología.

3.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo y volver al **Panel de topología**.

TopoEdit crea el nodo de transformación especificado. En el **Panel de topología** se muestra el nodo transformar como un cuadro verde que muestra el nombre de la MFT.

## <a name="to-add-a-custom-mft-to-the-topology"></a>Para agregar un MFT personalizado a la topología

1.  En el menú **topología** , haga clic en **Agregar MFT personalizado**.

    Se abrirá el cuadro de diálogo **GUID personalizado de entrada** .

2.  En el campo **GUID:** , escriba el GUID de la MFT que quiere agregar a la topología.

    > [!Note]  
    > TopoEdit espera el GUID con el formato "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}". De lo contrario, no se puede Agregar el nodo y se muestra un mensaje de error "GUID no válido".

     

3.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo y volver al **Panel de topología**.

TopoEdit crea el nodo de transformación especificado. En el **Panel de topología** se muestra el nodo transformar como un cuadro verde que muestra el nombre de la MFT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



