---
description: Establecimiento de las preferencias de desinteresación
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Establecimiento de las preferencias de desinteresación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33dae356618653f501b56f8b7a7eeb98e24ee92eb196cac78466e8cd26c01610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072579"
---
# <a name="setting-deinterlace-preferences"></a>Establecimiento de las preferencias de desinteresación

El representador de mezcla de vídeo (VMR) admite el desenlazado acelerado por hardware, lo que mejora la calidad de representación del vídeo entrelazado. Las características exactas que están disponibles dependen del hardware subyacente. La aplicación puede consultar las funcionalidades de desenlace de hardware y establecer preferencias de desenlace a través de la interfaz [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) o la interfaz [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9). El desinterlazado se realiza por secuencia.

Hay una diferencia importante en el comportamiento de entrelazado entre VMR-7 y VMR-9. En sistemas en los que el hardware gráfico no admite el desinterlazado avanzado, VMR-7 puede volver a la superposición de hardware e indicarle que use un desinterés de estilo BOB. En este caso, aunque vmr informa de 30 fps, el vídeo se representa realmente a 60 volteos por segundo.

Excepto en el caso del VMR-7 que usa la superposición de hardware, el mezclador de VMR realiza el desenlazado. El mezclador usa la interfaz del controlador de dispositivo (DDI) de desenlazado de aceleración de vídeo de DirectX (DXVA) para realizar el desenlazado. Las aplicaciones no pueden llamar a este DDI y las aplicaciones no pueden reemplazar la funcionalidad de desenlazado de VMR. Sin embargo, una aplicación puede seleccionar el modo de desenlazado deseado, como se describe en esta sección.

> [!Note]  
> En esta sección se describen los **métodos IVMRDeinterlaceControl9,** pero las versiones de VMR-7 son casi idénticas.

 

Para obtener las funcionalidades de desenlazado de una secuencia de vídeo, haga lo siguiente:

1.  Rellene una [**estructura VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) con una descripción de la secuencia de vídeo. Más adelante se detalla cómo rellenar esta estructura.
2.  Pase la estructura al [**método IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) Llame al método dos veces. La primera llamada devuelve el número de modos de desinterlace que admite el hardware para el formato especificado. Asigne una matriz de GUID de este tamaño y vuelva a llamar al método, pasando la dirección de la matriz. La segunda llamada rellena la matriz con GUID. Cada GUID identifica un modo de desenlazado.
3.  Para obtener las capacidades de un modo determinado, llame al método [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) Pase la misma **estructura VMR9VideoDesc,** junto con uno de los GUID de la matriz. El método rellena una estructura [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) con las funcionalidades de modo.

El siguiente código muestra estos pasos:


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



Ahora la aplicación puede establecer el modo de desenlazado para la secuencia mediante los métodos siguientes:

-   El [**método SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) establece el modo preferido. Use GUID \_ NULL para desactivar el desenlazado.
-   El [**método SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) especifica el comportamiento si el modo solicitado no está disponible.
-   El [**método GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) devuelve el modo preferido que se establece.
-   El [**método GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) devuelve el modo real en uso, que podría ser un modo de reserva, si el modo preferido no está disponible.

Las páginas de referencia de métodos dan más información.

**Uso de la estructura VMR9VideoDesc**

En el procedimiento anterior, el primer paso es rellenar una estructura **VMR9VideoDesc** con una descripción de la secuencia de vídeo. Empiece por obtener el tipo de medio de la secuencia de vídeo. Para ello, llame a [**IPin::ConnectionMediaType en**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) el pin de entrada del filtro de VMR. A continuación, confirme si la secuencia de vídeo está entrelazada. Solo se pueden entrelazar los formatos [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Si el tipo de formato es FORMAT \_ VideoInfo, debe ser un marco progresiva. Si el tipo de formato es FORMAT VideoInfo2, compruebe el \_ **campo dwInterlaceFlags** para la marca AMINTERLACE \_ IsInterlaced. La presencia de esta marca indica que el vídeo está entrelazado.

Suponga que la variable **pBMI** es un puntero a la [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el bloque de formato. Establezca los siguientes valores en la **estructura VMR9VideoDesc:**

-   **dwSize:** establezca este campo en `sizeof(VMR9VideoDesc)` .
-   **dwSampleWidth:** establezca este campo en `pBMI->biWidth` .
-   **dwSampleHeight:** establezca este campo en `abs(pBMI->biHeight)` .
-   **SampleFormat:** este campo describe las características de intercalación del tipo de medio. Compruebe el **campo dwInterlaceFlags en** la estructura **VIDEOINFOHEADER2** y establezca **SampleFormat** igual a la marca [**\_ SampleFormat de VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) equivalente. A continuación se ofrece una función auxiliar para hacerlo.
-   **InputSampleFreq:** este campo proporciona la frecuencia de entrada, que se puede calcular a partir del **campo AvgTimePerFrame** de la **estructura VIDEOINFOHEADER2.** En el caso general, establezca **dwNumerator** en 10000000 y **establezca dwDenominator** en **AvgTimePerFrame.** Sin embargo, también puede comprobar algunas velocidades de fotogramas conocidas:

    | Tiempo promedio por fotograma | Velocidad de fotogramas (fps) | Numerador | Denominador |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59.94 ( ESTO)     | 60000     | 1001        |
    | 333667                 | 29.97 ( ESTO)     | 30000     | 1001        |
    | 417188                 | 23.97 (CCA)     | 24000     | 1001        |
    | 200000                 | 50.00 (PAL)      | 50        | 1           |
    | 400000                 | 25.00 (PAL)      | 25        | 1           |
    | 416667                 | 24.00 (Película)     | 24        | 1           |

    

     

-   **OutputFrameFreq:** este campo proporciona la frecuencia de salida, que se puede calcular a partir del valor **InputSampleFreq** y las características de intercalación del flujo de entrada:
    -   Establezca **OutputFrameFreq.dwDenominator** en **InputSampleFreq.dwDenominator.**
    -   Si el vídeo de entrada está intercalado, establezca **OutputFrameFreq.dwNumerator** en 2 x **InputSampleFreq.dwNumerator.** (Después de desenlazar, se duplica la velocidad de fotogramas). De lo contrario, establezca el valor **en InputSampleFreq.dwNumerator.**
-   **dwFourCC:** establezca este campo en `pBMI->biCompression` .

La siguiente función auxiliar convierte las marcas AMINTERLACE \_ *X* en [**valores de VMR9 \_ SampleFormat:**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



