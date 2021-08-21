---
description: Implementación de IWICBitmapCodecProgressNotification (descodificador)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementación de IWICBitmapCodecProgressNotification (descodificador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff9af6bbd8c0457a5bf97f2f8b378cdeaca9269e792f7ed4696ab8e6a23b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088067"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementación de IWICBitmapCodecProgressNotification (descodificador)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Cuando un códec realiza una operación de E/S como [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en una imagen grande, puede tardar varios segundos o incluso minutos en completarse. Cuando los usuarios finales no pueden interrumpir una operación de ejecución larga, es posible que piensen que la aplicación se ha interrumpido. Los usuarios suelen cerrar una aplicación, o incluso reiniciar sus equipos, en un intento de recuperar el control de su equipo cuando una aplicación deja de responder.

Esta interfaz permite a una aplicación especificar una función de devolución de llamada a la que el códec puede llamar a intervalos especificados para notificar al autor de la llamada el progreso de la operación actual. La aplicación puede usar esta función de devolución de llamada para mostrar una indicación de progreso en la interfaz de usuario para notificar al usuario el estado de la operación. Si un usuario hace clic en el botón **Cancelar** del cuadro **de** diálogo Progreso, la aplicación devuelve **WINCODEC \_ ERR \_ ABORTED desde** la función de devolución de llamada. Cuando esto sucede, el códec debe cancelar la operación especificada y propagar este **HRESULT** de nuevo al llamador del método que estaba realizando la operación.

Esta interfaz debe implementarse en la clase descodificador de nivel de contenedor.


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**Una aplicación invoca RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) para registrar una función de devolución de llamada a la que el códec puede llamar a intervalos especificados. El primer parámetro, *pfnProgressNotification*, es un puntero a la función de devolución de llamada a la que el códec debe llamar a intervalos regulares.

El *parámetro pvData* apunta a algún objeto que el autor de la llamada desea que el códec vuelva a pasar a la función de devolución de llamada cada vez que se invoca la función de devolución de llamada. Este objeto puede ser cualquier cosa y no tiene ninguna importancia concreta para el códec.

El *parámetro dwProgressFlags* especifica cuándo debe llamar el códec a la función de devolución de llamada. Se puede realizar una función OR con dos enumeraciones para este parámetro. La enumeración [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) especifica si se debe llamar a la función de devolución de llamada durante la codificación **(WICProgressOperationCopyPixels),** la codificación (**WICProgerssOperationWritePixels)** o ambos **(WICProgressOperationAll).**


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



El códec debe llamar a la función de devolución de llamada a intervalos regulares a lo largo de la operación, pero el autor de la llamada puede especificar determinados requisitos. La [**enumeración WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica en qué punto de la operación se llama a la función de devolución de llamada. Si el autor de la llamada especifica **WICProgressNotificationBegin,** debe llamarlo al principio de la operación (0.0). Si el autor de la llamada no especifica esto, es opcional. Del mismo modo, si el autor de la llamada especifica **WICProgerssNotificationEnd,** debe llamarlo cuando se complete la operación (1.0). Si el autor de la llamada especifica **WICProgressNotificationAll,** debe llamarlo al principio y al final, así como a intervalos regulares a lo largo de la operación. El autor de la llamada también puede especificar **WICProgerssNotificationFrequent,** lo que indica que se quiere volver a llamar a intervalos frecuentes, quizás después de cada par de líneas de examen. (Normalmente, un autor de la llamada usará esta marca solo para una imagen muy grande). De lo contrario, normalmente debe volver a llamar a intervalos de incrementos aproximadamente del 10 % del número total de líneas de examen que se procesarán.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



Solo se puede registrar una función de devolución de llamada a la vez para un descodificador o una instancia de codificador específicos. Si una aplicación llama a [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) más de una vez, reemplace la función de devolución de llamada registrada anteriormente por la nueva. Para cancelar un registro de devolución de llamada, un llamador establecerá el *parámetro pfnProgressNotification* en **NULL.**

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification es**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) la función de devolución de llamada con la firma siguiente.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Al invocar la función de devolución de llamada, use el parámetro *pvData* para devolver el mismo *pvData* que la aplicación especificó cuando registró la función de devolución de llamada.

El *parámetro uFrameNum* debe indicar el índice del marco que se está procesando.

Establezca el parámetro operation en **WICProgressOperationCopyPixels** al codificar y **WICProgressOperationWritePixels** al codificar.

El *parámetro dblProgress* debe ser un número entre 0,0 (el principio de la operación) y 1,0 (la finalización de la operación). El valor debe reflejar la proporción de líneas de examen ya procesadas en relación con el número total de líneas de examen que se procesarán.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implementación de IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



