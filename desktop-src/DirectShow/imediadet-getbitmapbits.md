---
description: El método GetBitmapBits recupera un fotograma de vídeo en el tiempo medio especificado. El marco devuelto siempre tiene el formato RGB de 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'IMediaDet:: GetBitmapBits (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680964"
---
# <a name="imediadetgetbitmapbits-method"></a>IMediaDet:: GetBitmapBits (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetBitmapBits` método recupera un fotograma de vídeo en el tiempo medio especificado. El marco devuelto siempre tiene el formato RGB de 24 bits.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StreamTime* 
</dt> <dd>

Hora a la que se va a recuperar el fotograma de vídeo, en segundos.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Recibe el tamaño de búfer necesario. Si *pBuffer* es **null**, la variable recibe el tamaño del búfer necesario para recuperar el marco. Si *pBuffer* no es **null**, se omite este parámetro.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntero a un búfer que recibe una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguido de los bits Dib.

</dd> <dt>

*Width* 
</dt> <dd>

Ancho de la imagen de vídeo, en píxeles.

</dd> <dt>

*Height* 
</dt> <dd>

Alto de la imagen de vídeo, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                             | Descripción                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                                                               |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | No se pudo agregar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) al gráfico.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insuficiente.<br/>                                                                   |
| <dl> <dt>**\_puntero E**</dt> </dl>               | Error de puntero **nulo** .<br/>                                                                |
| <dl> <dt>**E \_ inesperado**</dt> </dl>            | error inesperado.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                                                                    |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Para determinar el tamaño del búfer necesario, llame a este método con *pBuffer* igual a **null**. El tamaño se devuelve en la variable a la que apunta *pBufferSize*. A continuación, cree el búfer y llame de nuevo al método, con *pBuffer* igual a la dirección del búfer. Cuando el método devuelve, el búfer contiene una estructura **BITMAPINFOHEADER** seguida del mapa de bits. El mapa de bits se escala a las dimensiones especificadas en los parámetros *ancho* y *alto* .

Este método coloca el detector de medios en el modo de agarre de mapa de bits. Una vez que se ha llamado a este método, los distintos métodos de información de secuencia de **IMediaDet** no funcionan, a menos que cree una nueva instancia del detector de medios.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Ejemplos

En el código siguiente se usa el `GetBitmapBits` método para crear un mapa de bits independiente del dispositivo.


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




