---
description: Los mapas de bits dependientes del dispositivo (DDB) se describen mediante una sola estructura, la estructura BITMAP.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Device-Dependent mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cf365b0f3b11e4a79bb0e7b1e1749d75ca356d41454e40cc6c31f383a74701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887246"
---
# <a name="device-dependent-bitmaps"></a>Device-Dependent mapa de bits

Los mapas de bits dependientes del dispositivo (DDB) se describen mediante una sola estructura, la [**estructura BITMAP.**](/windows/win32/api/wingdi/ns-wingdi-bitmap) Los miembros de esta estructura especifican el ancho y el alto de una región rectangular, en píxeles; el ancho de la matriz que asigna entradas de la paleta de dispositivos a píxeles; y el formato de color del dispositivo, en términos de planos de color y bits por píxel. Una aplicación puede recuperar el formato de color de un dispositivo llamando a la [**función GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especificando las constantes adecuadas. Tenga en cuenta que una DDB no contiene valores de color; en su lugar, los colores están en un formato dependiente del dispositivo. Para obtener más información, [vea Color in Bitmaps](color-in-bitmaps.md). Dado que cada dispositivo puede tener su propio conjunto de colores, es posible que una DDB creada para un dispositivo no se muestre bien en otro dispositivo.

Para usar una DDB en un contexto de dispositivo, debe tener la organización de color de ese contexto de dispositivo. Por lo tanto, una DDB a menudo se denomina mapa de *bits compatible* y normalmente tiene un mejor rendimiento de GDI que una DIB. Por ejemplo, para crear un mapa de bits para la memoria de vídeo, es mejor usar un mapa de bits compatible con el mismo formato de color que la pantalla principal. Una vez en la memoria de vídeo, la representación en el mapa de bits y su visualización en la pantalla son significativamente más rápidas que desde una superficie de memoria del sistema o directamente desde una DIB.

Además de habilitar un mejor rendimiento de GDI, los mapas de bits compatibles se usan para capturar imágenes (consulte [Captura](capturing-an-image.md) de una imagen) y para crear mapas de bits en tiempo de ejecución para los menús, vea "Crear el mapa de bits" en (vea Usar [menús).](../menurc/using-menus.md)

Para transferir un mapa de bits entre dispositivos con una organización de color diferente, use [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) para convertir el mapa de bits compatible en una DIB y llame a [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) para mostrar la DIB en el segundo dispositivo.

Hay dos tipos de DDB: descartables y no descartables. Una DDB descartable es un mapa de bits que el sistema descarta si el mapa de bits no está seleccionado en un controlador de dominio y si la memoria del sistema es baja. La [**función CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) crea mapas de bits descartables. Las [**funciones CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateCompatibleBitmap y**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) crean mapas de bits no intercambiables.

Una aplicación puede crear una DDB a partir de una DIB inicializando las estructuras necesarias y llamando a [**la función CreateDIBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) Especificar CBM INIT en la llamada \_ a **CreateDIBitmap** equivale a llamar a la función [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) para crear una DDB en el formato del dispositivo y, a continuación, llamar a la función [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) para traducir los bits DIB a DDB. Para determinar si un dispositivo admite la función **SetDIBits,** llame a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especifique RC DI BITMAP como marca \_ \_ RASTERCAPS.

 

 
