---
description: Los mapas de bits dependientes del dispositivo (DDBs) se describen mediante una única estructura, la estructura de mapa de bits.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Mapas de bits Device-Dependent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a3de2c59509c71b38f9981df330b3b28effa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155644"
---
# <a name="device-dependent-bitmaps"></a>Mapas de bits Device-Dependent

Los mapas de bits dependientes del dispositivo (DDBs) se describen mediante una única estructura, la estructura de [**mapa de bits**](/windows/win32/api/wingdi/ns-wingdi-bitmap) . Los miembros de esta estructura especifican el ancho y el alto de una región rectangular, en píxeles; ancho de la matriz que asigna las entradas de la paleta del dispositivo a píxeles; y el formato de color del dispositivo, en términos de planos de color y bits por píxel. Una aplicación puede recuperar el formato de color de un dispositivo llamando a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especificando las constantes adecuadas. Tenga en cuenta que un DDB no contiene valores de color; en su lugar, los colores se encuentran en un formato dependiente del dispositivo. Para obtener más información, vea [color en mapas de bits](color-in-bitmaps.md). Dado que cada dispositivo puede tener su propio conjunto de colores, es posible que un DDB creado para un dispositivo no se muestre correctamente en un dispositivo diferente.

Para usar DDB en un contexto de dispositivo, debe tener la organización de color de ese contexto de dispositivo. Por lo tanto, un DDB se denomina a menudo un *mapa de bits compatible* y normalmente tiene mejor rendimiento de GDI que un Dib. Por ejemplo, para crear un mapa de bits para la memoria de vídeo, es mejor usar un mapa de bits compatible con el mismo formato de color que la pantalla principal. Una vez en la memoria de vídeo, la representación en el mapa de bits y su visualización en la pantalla son significativamente más rápidas que en una superficie de memoria del sistema o directamente desde un DIB.

Además de habilitar mejor el rendimiento de GDI, se usan mapas de bits compatibles para capturar imágenes (vea [capturar una imagen](capturing-an-image.md) ) y para crear mapas de bits en tiempo de ejecución para los menús, vea "crear el mapa de bits" en (vea [usar menús](../menurc/using-menus.md) ).

Para transferir un mapa de bits entre dispositivos con una organización de color diferente, use [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) para convertir el mapa de bits compatible en un DIB y llamar a [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) para mostrar el DIB en el segundo dispositivo.

Hay dos tipos de DDBs: descartable y no descartable. Un DDB descartable es un mapa de bits que descarta el sistema si el mapa de bits no está seleccionado en un controlador de dominio y si la memoria del sistema es baja. La función [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) crea mapas de bits descartables. Las funciones [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)y [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) crean mapas de bits no descartables.

Una aplicación puede crear un DDB a partir de un DIB Inicializando las estructuras necesarias y llamando a la función [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) . La especificación de \_ la inicialización ABLC en la llamada a **CreateDIBitmap** es equivalente a llamar a la función [**CREATECOMPATIBLEBITMAP**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) para crear un DDB en el formato del dispositivo y, a continuación, llamar a la función [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) para traducir los bits DIB a DDB. Para determinar si un dispositivo admite la función **SetDIBits** , llame a la función [**GETDEVICECAPS**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especifique RC \_ di \_ Bitmap como marca RASTERCAPS.

 

 
