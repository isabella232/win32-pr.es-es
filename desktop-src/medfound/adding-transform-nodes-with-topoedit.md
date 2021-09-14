---
description: Agregar nodos de transformación con TopoEdit
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: Agregar nodos de transformación con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fa39457f8808070f93a4e5de31e181525ca33b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269423"
---
# <a name="adding-transform-nodes-with-topoedit"></a>Agregar nodos de transformación con TopoEdit

Un nodo de transformación representa un Media Foundation transformación (MFT) que procesa los datos multimedia que recibe de un nodo de origen. Cuando está lista, la canalización la pasa al nodo de salida para su representación. En Media Foundation, los codificadores, descodificadores, multiplexores, des multiplexores y efectos de vídeo de audio se implementan como MTA. TopoEdit admite la adición de nodos de transformación que representan MTA registrados y personalizados.

Para obtener información sobre cómo agregar nodos de transformación mediante programación mediante Media Foundation API, vea [Crear nodos de transformación](creating-transform-nodes.md).

## <a name="to-add-a-registered-mft-to-the-topology"></a>Para agregar un MFT registrado a la topología

1.  En el **menú Topología,** haga clic **en Agregar transformación.**

    Se **abre el cuadro de** diálogo Seleccionar transformación. Muestra una lista categorizada de MFTT registrados que se genera enumerando las entradas registradas en el Registro mediante una llamada a la [**función MFTEnum.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)

2.  Expanda la categoría y seleccione el MFT que desea agregar a la topología.

3.  Haga **clic en** Aceptar para cerrar el cuadro de diálogo y volver al panel **Topología**.

TopoEdit crea el nodo de transformación especificado. El **panel Topología muestra** el nodo de transformación como un cuadro verde que muestra el nombre del MFT.

## <a name="to-add-a-custom-mft-to-the-topology"></a>Para agregar un MFT personalizado a la topología

1.  En el **menú Topología,** haga clic **en Agregar MFT personalizado.**

    Se abre el cuadro **de diálogo GUID personalizado** de entrada.

2.  En el **campo GUID:** , escriba el GUID del MFT que desea agregar a la topología.

    > [!Note]  
    > TopoEdit espera el GUID con el formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". De lo contrario, no se puede agregar el nodo y se muestra un mensaje de error "GUID no válido".

     

3.  Haga **clic en** Aceptar para cerrar el cuadro de diálogo y volver al panel **Topología**.

TopoEdit crea el nodo de transformación especificado. El **panel Topología muestra** el nodo de transformación como un cuadro verde que muestra el nombre del MFT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



