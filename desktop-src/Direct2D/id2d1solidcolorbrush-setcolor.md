---
title: Métodos de ID2D1SolidColorBrush SetColor
description: Especifica el color de este pincel de color sólido.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Métodos de SetColor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680841"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>ID2D1SolidColorBrush:: SetColor (métodos)

Especifica el color de este pincel de color sólido.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                          | Descripción                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor (D2D1 de \_ color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Especifica el color de este pincel de color sólido. <br/> |
| [**SetColor (D2D1 de \_ color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Especifica el color de este pincel de color sólido. <br/> |



## <a name="remarks"></a>Observaciones

Para ayudar a crear colores, Direct2D proporciona la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) . Ofrece varios métodos auxiliares para crear colores y proporciona un conjunto o colores predefinidos.

## <a name="examples"></a>Ejemplos

En el código siguiente se muestra cómo utilizar este método.


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

