---
description: El método GetBitmapBits recupera un fotograma de vídeo en el momento del medio especificado. El marco devuelto siempre está en formato RGB de 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: Método IMediaDet::GetBitmapBits (Qedit.h)
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
ms.openlocfilehash: 5c4a7332580d4e9a9fece5a66d390753566fbf54c615699663256c463cb401b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792005"
---
# <a name="imediadetgetbitmapbits-method"></a>IMediaDet::GetBitmapBits (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetBitmapBits` método recupera un fotograma de vídeo en el momento del medio especificado. El marco devuelto siempre está en formato RGB de 24 bits.

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

Recibe el tamaño de búfer necesario. Si *pBuffer* es **NULL,** la variable recibe el tamaño del búfer necesario para recuperar el marco. Si *pBuffer* no es **NULL,** se omite este parámetro.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntero a un búfer que recibe una [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguida de los bits DIB.

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

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                             | Descripción                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | No se pudo agregar el [**filtro Sample Grabber**](sample-grabber-filter.md) al gráfico.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insuficiente.<br/>                                                                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Error de** puntero NULL.<br/>                                                                |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | error inesperado.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                                                                    |



 

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, establezca el nombre de archivo y la secuencia llamando a [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Para determinar el tamaño del búfer necesario, llame a este método con *pBuffer* igual a **NULL.** El tamaño se devuelve en la variable a la que apunta *pBufferSize*. A continuación, cree el búfer y vuelva a llamar al método , con *pBuffer* igual a la dirección del búfer. Cuando el método devuelve un resultado, el búfer contiene una **estructura BITMAPINFOHEADER** seguida del mapa de bits. El mapa de bits se escala a las dimensiones especificadas en los *parámetros Width* *y Height.*

Este método coloca el detector de medios en modo de captura de mapa de bits. Una vez que se ha llamado a este método, los distintos métodos de información de secuencias de **IMediaDet** no funcionan, a menos que cree una nueva instancia del detector de medios.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="examples"></a>Ejemplos

El código siguiente usa el `GetBitmapBits` método para crear un mapa de bits independiente del dispositivo.


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
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




