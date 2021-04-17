---
description: La clase CSeekingPassThru es un objeto auxiliar que crea objetos CPosPassThru y CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Clase CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690002"
---
# <a name="cseekingpassthru-class"></a>Clase CSeekingPassThru

La `CSeekingPassThru` clase es un objeto auxiliar que crea objetos [**CPosPassThru**](cpospassthru.md) y [**CRendererPosPassThru**](crendererpospassthru.md) .

Las clases **CPosPassThru** y **CRendererPosPassThru** son objetos auxiliares que pasan los comandos de búsqueda ascendentes, por lo que la `CSeekingPassThru` clase es un objeto auxiliar para crear objetos auxiliares.

No es necesario usar esta clase directamente. En su lugar, use la función [**CreatePosPassThru**](createpospassthru.md) , que controla todos los detalles del uso de esta clase. Tiene más ventajas de cargar el objeto desde Quartz.dll, lo que reduce ligeramente el tamaño del código del filtro. Para obtener más información, vea [**CPosPassThru**](cpospassthru.md).

La `CSeekingPassThru` clase expone la interfaz [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) . El método [**ISeekingPassThru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) inicializa el objeto. Una vez inicializado el objeto, el filtro puede consultarlo para las interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) y [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .



| Métodos públicos                                                  | Descripción                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Método de constructor.                |
| [**~ CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Método de destructor.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Crea una instancia del objeto. |
| Métodos ISeekingPassThru                                        | Descripción                        |
| [**Smss**](cseekingpassthru-init.md)                           | Inicializa el objeto.            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Seekpt. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




