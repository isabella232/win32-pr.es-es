---
description: Búferes de vídeo sin comprimir
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Búferes de vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696867"
---
# <a name="uncompressed-video-buffers"></a>Búferes de vídeo sin comprimir

En este artículo se describe cómo trabajar con búferes multimedia que contienen fotogramas de vídeo sin comprimir. En orden de preferencia, están disponibles las siguientes opciones. No todos los búferes multimedia admiten cada opción.

1.  Usar la superficie de Direct3D subyacente. (Se aplica solo a fotogramas de vídeo almacenados en superficies de Direct3D).
2.  Use la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
3.  Use la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .

## <a name="use-the-underlying-direct3d-surface"></a>Usar la superficie de Direct3D subyacente

El fotograma de vídeo puede almacenarse dentro de una superficie de Direct3D. Si es así, puede obtener un puntero a la superficie llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) o [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el objeto de búfer de multimedia. Use el servicio de búfer del identificador de servicio MR \_ \_ . Se recomienda este enfoque cuando el componente que tiene acceso al fotograma de vídeo está diseñado para usar Direct3D. Por ejemplo, un descodificador de vídeo compatible con la aceleración de vídeo de DirectX debe utilizar este enfoque.

En el código siguiente se muestra cómo obtener el puntero **IDirect3DSurface9** desde un búfer multimedia.


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



Los objetos siguientes admiten el servicio de **\_ \_ servicio de búfer Mr** :

-   [Búfer de superficie de DirectX](directx-surface-buffer.md)
-   [Ejemplos de vídeo](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>Uso de la interfaz IMF2DBuffer

Si el fotograma de vídeo no se almacena en una superficie de Direct3D, o el componente no está diseñado para usar Direct3D, la siguiente manera recomendada de acceder al fotograma de vídeo es consultar el búfer para la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Esta interfaz está diseñada específicamente para los datos de imagen. Para obtener un puntero a esta interfaz, llame a **QueryInterface** en el búfer multimedia. No todos los objetos de búfer multimedia exponen esta interfaz. Pero si un búfer multimedia expone la interfaz **IMF2DBuffer** , debe usar esa interfaz para tener acceso a los datos, si es posible, en lugar de usar [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer). Todavía puede usar la interfaz **IMFMediaBuffer** , pero podría ser menos eficaz.

1.  Llame a **QueryInterface** en el búfer multimedia para obtener la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
2.  Llame a [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para tener acceso a la memoria del búfer. Este método devuelve un puntero al primer byte de la fila superior de píxeles. También devuelve el paso de la imagen, que es el número de bytes desde el inicio de una fila de píxeles hasta el inicio de la siguiente fila. El búfer puede contener bytes de relleno después de cada fila de píxeles, por lo que el intervalo puede ser más ancho que el ancho de la imagen en bytes. STRIDE también puede ser negativo si la imagen está orientada en orden ascendente en la memoria. Para obtener más información, consulte [STRIDE](image-stride.md)de la imagen.
3.  Mantenga el búfer bloqueado solo mientras necesite tener acceso a la memoria. Desbloquee el búfer mediante una llamada a [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).

No todos los búferes multimedia implementan la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Si el búfer multimedia no implementa esta interfaz (es decir, el objeto de búfer devuelve E \_ nointerface en el paso 1), debe usar la interfaz de la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , que se describe a continuación.

## <a name="use-the-imfmediabuffer-interface"></a>Uso de la interfaz IMFMediaBuffer

Si un búfer multimedia no expone la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . La semántica general de esta interfaz se describe en el tema [trabajar con búferes multimedia](working-with-media-buffers.md).

1.  Llame a **QueryInterface** en el búfer multimedia para obtener la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
2.  Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para tener acceso a la memoria del búfer. Este método devuelve un puntero a la memoria del búfer. Cuando se usa el método de **bloqueo** , el intervalo es siempre el intervalo mínimo para el formato de vídeo en cuestión, sin bytes adicionales de relleno.
3.  Mantenga el búfer bloqueado solo mientras necesite tener acceso a la memoria. Desbloquee el búfer mediante una llamada a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Siempre debe evitar llamar a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) si el búfer expone [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), ya que el método **Lock** puede forzar el objeto de búfer al fotograma de vídeo en un bloque de memoria contiguo y después volver de nuevo. Por otro lado, si el búfer no es compatible con **IMF2DBuffer**, probablemente **IMFMediaBuffer:: Lock** no producirá una copia.

Calcule el intervalo mínimo del tipo de medio como se indica a continuación:

-   El intervalo mínimo puede almacenarse en el atributo de [**\_ \_ \_ intervalo MF MT predeterminado**](mf-mt-default-stride-attribute.md) .
-   Si no se ha establecido el atributo de **\_ \_ \_ intervalo MF MT predeterminado** , llame a la función [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) para calcular el intervalo para los formatos de vídeo más comunes.
-   Si la función [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) no reconoce el formato, debe calcular el intervalo en función de la definición del formato. En ese caso, no hay ninguna regla general; necesita conocer los detalles de la definición de formato.

En el código siguiente se muestra cómo obtener el intervalo predeterminado para los formatos de vídeo más comunes.


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



En función de la aplicación, puede saber de antemano si un búfer multimedia determinado admite [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (por ejemplo, si ha creado el búfer). De lo contrario, debe estar preparado para usar cualquiera de las dos interfaces de búfer.

En el ejemplo siguiente se muestra una clase auxiliar que oculta algunos de estos detalles. Esta clase tiene un método LockBuffer que llama a [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) o [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) y devuelve un puntero al principio de la primera fila de píxeles. (Este comportamiento coincide con el método **Lock2D** ). El método LockBuffer toma el intervalo predeterminado como parámetro de entrada y devuelve el intervalo real como parámetro de salida.


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Intervalo de imagen](image-stride.md)
</dt> <dt>

[Búferes multimedia](media-buffers.md)
</dt> </dl>

 

 



