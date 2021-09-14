---
description: La clase CSeekingPassThru es un objeto auxiliar que crea objetos CPosPassThru y CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: CSeekingPassThru (clase, Seekpt.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070048"
---
# <a name="cseekingpassthru-class"></a>CSeekingPassThru (clase)

La `CSeekingPassThru` clase es un objeto auxiliar que crea objetos [**CPosPassThru**](cpospassthru.md) y [**CRendererPosPassThru.**](crendererpospassthru.md)

Las **clases CPosPassThru** y **CRendererPosPassThru** son objetos auxiliares que pasan comandos de búsqueda ascendentes, por lo que la clase es un objeto auxiliar para crear `CSeekingPassThru` objetos auxiliares.

No es necesario usar esta clase directamente. En su lugar, use [**la función CreatePosPassThru,**](createpospassthru.md) que controla todos los detalles del uso de esta clase. Tiene la ventaja adicional de cargar el objeto desde Quartz.dll, lo que reduce ligeramente el tamaño del código del filtro. Para obtener más información, [**vea CPosPassThru**](cpospassthru.md).

La `CSeekingPassThru` clase expone la interfaz [**ISeekingPassThru.**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) El [**método ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) inicializa el objeto . Una vez inicializado el objeto, el filtro puede consultarlo para las interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**e IMediaPosition.**](/windows/desktop/api/Control/nn-control-imediaposition)



| Métodos públicos                                                  | Descripción                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Método constructor.                |
| [**~CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Método destructor.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Crea una instancia del objeto . |
| ISeekingPassThru (métodos)                                        | Descripción                        |
| [**Init**](cseekingpassthru-init.md)                           | Inicializa el objeto.            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Seekpt.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




