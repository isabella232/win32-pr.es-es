---
description: Establecer preferencias de desentrelazado
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Establecer preferencias de desentrelazado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805204"
---
# <a name="setting-deinterlace-preferences"></a>Establecer preferencias de desentrelazado

El representador de mezcla de vídeo (VMR) admite desentrelazado acelerado por hardware, lo que mejora la calidad de representación de vídeo entrelazado. Las características exactas que están disponibles dependen del hardware subyacente. La aplicación puede consultar las funcionalidades de desentrelazado de hardware y establecer preferencias de desentrelazado a través de la interfaz [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) o de la interfaz [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9). El desentrelazado se realiza por secuencia.

Existe una diferencia importante en el comportamiento de entrelazado entre el VMR-7 y el VMR-9. En los sistemas en los que el hardware gráfico no admite el desentrelazado avanzado, VMR-7 puede revertir a la superposición de hardware y indicarle que use un desentrelazado de estilo BOB. En este caso, aunque el VMR está informando de 30 fps, el vídeo se está representando realmente en 60 volteo por segundo.

Excepto en el caso de VMR-7 mediante la superposición de hardware, el mezclador de VMR realiza el desentrelazado. El mezclador usa la interfaz de controlador de dispositivo (DDI) de desentrelazado de DirectX video Acceleration (DXVA) para realizar el desentrelazado. Las aplicaciones no pueden llamar a este DDI y las aplicaciones no pueden reemplazar la funcionalidad de desentrelazado de VMR. Sin embargo, una aplicación puede seleccionar el modo de desentrelazado deseado, tal como se describe en esta sección.

> [!Note]  
> En esta sección se describen los métodos de **IVMRDeinterlaceControl9** , pero las versiones de VMR-7 son casi idénticas.

 

Para obtener las capacidades de desentrelazado de una secuencia de vídeo, haga lo siguiente:

1.  Rellene una estructura [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) con una descripción de la secuencia de vídeo. Más adelante se proporcionan detalles sobre cómo rellenar esta estructura.
2.  Pase la estructura al método [**IVMRDeinterlaceControl9:: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) . Llame al método dos veces. La primera llamada devuelve el número de modos de desentrelazado que el hardware admite para el formato especificado. Asigne una matriz de GUID de este tamaño y llame de nuevo al método, pasando la dirección de la matriz. La segunda llamada rellena la matriz con GUID. Cada GUID identifica un modo de desentrelazado.
3.  Para obtener el funcionalidades de un modo determinado, llame al método [**IVMRDeinterlaceControl9:: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) . Pase la misma estructura **VMR9VideoDesc** , junto con uno de los GUID de la matriz. El método rellena una estructura [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) con las capacidades de modo.

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



Ahora la aplicación puede establecer el modo de desentrelazado para el flujo, mediante los métodos siguientes:

-   El método [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) establece el modo preferido. Use GUID \_ null para desactivar el desentrelazado.
-   El método [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) especifica el comportamiento si el modo solicitado no está disponible.
-   El método [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) devuelve el modo preferido que establezca.
-   El método [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) devuelve el modo real en uso, que puede ser un modo de reserva, si el modo preferido no está disponible.

Las páginas de referencia de método proporcionan más información.

**Uso de la estructura VMR9VideoDesc**

En el procedimiento dado anteriormente, el primer paso es rellenar una estructura **VMR9VideoDesc** con una descripción de la secuencia de vídeo. Empiece obteniendo el tipo de medio de la secuencia de vídeo. Para ello, puede llamar a [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) en el PIN de entrada del filtro VMR. A continuación, confirme si la secuencia de vídeo está entrelazada. Solo se pueden entrelazar los formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Si el tipo de formato es FORMAT \_ info, debe ser un fotograma progresivo. Si el tipo de formato es \_ VideoInfo2, compruebe el campo **dwInterlaceFlags** para la \_ marca AMINTERLACE IsInterlaced. La presencia de esta marca indica que el vídeo está entrelazado.

Supongamos que la variable **pBMI** es un puntero a la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el bloque Format. Establezca los siguientes valores en la estructura **VMR9VideoDesc** :

-   **dwSize**: establezca este campo en `sizeof(VMR9VideoDesc)` .
-   **dwSampleWidth**: establezca este campo en `pBMI->biWidth` .
-   **dwSampleHeight**: establezca este campo en `abs(pBMI->biHeight)` .
-   **SampleFormat**: este campo describe las características de entrelazado del tipo de medio. Compruebe el campo **dwInterlaceFlags** en la estructura **VIDEOINFOHEADER2** y establezca **SampleFormat** en el valor de la marca [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) equivalente. A continuación se proporciona una función auxiliar para hacerlo.
-   **InputSampleFreq**: este campo proporciona la frecuencia de entrada, que se puede calcular a partir del campo **AvgTimePerFrame** de la estructura **VIDEOINFOHEADER2** . En el caso general, establezca **dwNumerator** en 10 millones y establezca **dwDenominator** en **AvgTimePerFrame**. Sin embargo, también puede buscar algunas velocidades de fotogramas conocidas:

    | Promedio de tiempo por fotograma | Velocidad de fotogramas (FPS) | Numera | Denominador |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59,94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29,97 (NTSC)     | 30000     | 1001        |
    | 417188                 | 23,97 (NTSC)     | 24000     | 1001        |
    | 200000                 | 50,00 (PAL)      | 50        | 1           |
    | 400000                 | 25,00 (PAL)      | 25        | 1           |
    | 416667                 | 24,00 (película)     | 24        | 1           |

    

     

-   **OutputFrameFreq**: este campo proporciona la frecuencia de salida, que se puede calcular a partir del valor **InputSampleFreq** y las características de intercalación del flujo de entrada:
    -   Establezca **OutputFrameFreq. dwDenominator** en **InputSampleFreq. dwDenominator**.
    -   Si el vídeo de entrada está entrelazado, establezca **OutputFrameFreq. dwNumerator** en 2 x **InputSampleFreq. dwNumerator**. (Después de desentrelazar, se duplica la velocidad de fotogramas). De lo contrario, establezca el valor en **InputSampleFreq. dwNumerator**.
-   **dwFourCC**: establezca este campo en `pBMI->biCompression` .

La siguiente función auxiliar convierte marcas AMINTERLACE \_ *X* en valores [**\_ SampleFormat de VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :


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



 

 



