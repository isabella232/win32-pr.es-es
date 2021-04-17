---
description: La clase CUnknown implementa la interfaz IUnknown. La mayoría de los objetos del modelo de objetos componentes (COM) de DirectShow se derivan de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Clase CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680875"
---
# <a name="cunknown-class"></a>Clase CUnknown

![jerarquía de clases cunknown](images/cbase01.png)

La clase **CUnknown** implementa la interfaz **IUnknown** . La mayoría de los objetos del modelo de objetos componentes (COM) de DirectShow se derivan de **CUnknown**.

Si implementa un objeto COM, puede que desee derivarlo de **CUnknown**. La derivación de **CUnknown** proporciona una implementación segura para subprocesos y evita el problema de implementar **IUnknown**.

Para obtener una explicación detallada sobre cómo usar esta clase base, vea [How to implement IUnknown](how-to-implement-iunknown.md). A continuación se muestra un breve resumen:

-   Incluya la macro [**declare \_ IUNKNOWN**](declare-iunknown.md) en la sección Public de la definición de clase. Esta macro declara los tres métodos de la interfaz **IUnknown** .
-   Invalide el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para admitir interfaces que no sean **IUnknown**. Dentro de este método, llame a la función [**GetInterface**](getinterface.md) para recuperar punteros de interfaz.
-   En el constructor de clase, invoque el método de constructor **CUnknown** .



| Variables de miembro protegidas                                                  | Descripción                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m \_ cRef**](cunknown-m-cref.md)                                          | Recuento de referencias.                                                   |
| Métodos públicos                                                              | Descripción                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Método de constructor.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Método de destructor. Virtualiza.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Obtiene un puntero al **IUnknown** de control.                    |
| Métodos INonDelegatingUnknown                                               | Descripción                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Incrementa el recuento de referencias.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Recupera un puntero de interfaz e incrementa el recuento de referencias. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Disminuye el recuento de referencias.                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




