---
title: Métodos SetTransform de ID2D1Brush (D2d1 \_ 1.h)
description: Establece la transformación aplicada al pincel.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Métodos SetTransform de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a5a30d4051303667402fdd1143f5a813d7515223c8093a5913294e6dd1722273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918045"
---
# <a name="id2d1brushsettransform-methods"></a>Métodos ID2D1Brush::SetTransform

Establece la transformación aplicada al pincel.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                       | Descripción                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Establece la transformación aplicada al pincel.<br/> |
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Establece la transformación aplicada al pincel.<br/> |



## <a name="remarks"></a>Comentarios

Cuando se pinta con un pincel, se pinta en el espacio de coordenadas del destino de representación. Los pinceles no se posicionan automáticamente para alinearse con el objeto que se está pintando. De forma predeterminada, comienzan a pintar en el origen (0, 0) del destino de representación.

Puede "mover" el degradado definido por [**id2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) a un área de destino estableciendo su punto inicial y punto final. Del mismo modo, puede mover el degradado definido por [**un ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando su centro y sus radii.

Para alinear el contenido de [**un objeto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con el área que se está pintando, puede usar el método **SetTransform** para traducir el mapa de bits a la ubicación deseada. Esta transformación solo afecta al pincel; no afecta a ningún otro contenido dibujado por el destino de representación.

En las ilustraciones siguientes se muestra el efecto de usar [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para rellenar un rectángulo ubicado en (100, 100). La ilustración de la izquierda muestra el resultado de rellenar el rectángulo sin transformar el pincel: el mapa de bits se dibuja en el origen del destino de representación. Como resultado, solo aparece una parte del mapa de bits en el rectángulo.

En la ilustración de la derecha se muestra el resultado de transformar [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para que su contenido se desplaza 50 píxeles hacia la derecha y 50 píxeles hacia abajo. El mapa de bits ahora rellena el rectángulo.

![ilustración de dos cuadrados, uno con un mapa de bits sin un pincel transformado y otro con un pincel transformado](images/brushes-ovw-transform.png)

## <a name="examples"></a>Ejemplos

En los ejemplos de código siguientes se muestra cómo crear la transformación que se muestra en el diagrama derecho de la ilustración anterior. En primer lugar, aplique una traducción a [**ID2D1BitmapBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)moviendo el pincel 50 píxeles a la derecha a lo largo del eje X y 50 píxeles hacia abajo a lo largo del eje Y. A continuación, use **ID2D1BitmapBrush** para rellenar el rectángulo que tiene la esquina superior izquierda en (100, 100) y la esquina inferior derecha en (200, 200).


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1 \_ 1.h (incluir D2d1.h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
