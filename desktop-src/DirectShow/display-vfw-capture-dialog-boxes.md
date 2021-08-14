---
description: Mostrar cuadros de diálogo de captura de VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Mostrar cuadros de diálogo de captura de VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2713cc4d2eba52626c66974eed23f2c1752a1268fea78a30ca2bc9d7babc3a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821143"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Mostrar cuadros de diálogo de captura de VFW

Un dispositivo de captura que todavía usa un controlador Video for Windows (VFW) puede admitir cualquiera de los tres cuadros de diálogo siguientes, que se usan para configurar el dispositivo.



| Cuadro de diálogo    | Descripción                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Origen de vídeo  | Se usa para seleccionar la entrada de vídeo y ajustar la configuración del dispositivo, como el brillo o el contraste de la imagen. |
| Formato de vídeo  | Se usa para seleccionar las dimensiones de imagen y la profundidad de bits.                                                    |
| Visualización de vídeo | Se usa para controlar la apariencia del vídeo representado.                                                 |



 

Para mostrar uno de estos cuadros de diálogo, haga lo siguiente:

1.  Detenga el gráfico de filtro.
2.  Consulte el filtro de captura para la [**interfaz IAMVfwCaptureDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) Si **QueryInterface se** realiza correctamente, significa que el dispositivo de captura es un dispositivo VFW.
3.  Llame [**a IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) para comprobar si el controlador admite el cuadro de diálogo que desea mostrar. La [**enumeración VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) define marcas para cada uno de los cuadros de diálogo vfw. **HasDialog** devuelve S \_ OK si se admite el cuadro de diálogo. De lo contrario, devuelve S FALSE, así que compruebe el valor S OK directamente, en \_ lugar de usar la macro \_ **SUCCEEDED.**
4.  Si se admite el cuadro de diálogo, llame a [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) para mostrar el cuadro de diálogo.
5.  Reinicie el gráfico.

El código siguiente muestra estos pasos para el cuadro de diálogo Origen de vídeo:


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de un dispositivo de captura de vídeo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



