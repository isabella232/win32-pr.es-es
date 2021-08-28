---
description: La clase CUnknown implementa la interfaz IUnknown. La mayoría de los objetos del Modelo de objetos componentes (COM) DirectShow derivan de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: CUnknown (clase, Combase.h)
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
ms.openlocfilehash: 06b6089f7f1c108a9b99ad4f1b16f4638b84d8d687a3590353c32841ccfff499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076005"
---
# <a name="cunknown-class"></a>CUnknown (clase)

![jerarquía de clases cunknown](images/cbase01.png)

La **clase CUnknown** implementa la **interfaz IUnknown.** La mayoría de los objetos del Modelo de objetos componentes (COM) DirectShow derivan **de CUnknown**.

Si implementa un objeto COM, es posible que desee derivarlo de **CUnknown**. Derivar de **CUnknown** proporciona una implementación segura para subprocesos y le ahorra el problema de implementar **IUnknown.**

Para obtener una explicación detallada de cómo usar esta clase base, vea [How to Implement IUnknown](how-to-implement-iunknown.md). A continuación se muestra un breve resumen:

-   Incluya la [**macro DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la sección public de la definición de clase. Esta macro declara los tres métodos de la **interfaz IUnknown.**
-   Invalide [**el método NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para admitir interfaces que no **son IUnknown.** Dentro de este método, llame a la [**función GetInterface**](getinterface.md) para recuperar punteros de interfaz.
-   En el constructor de clase, invoque el método de constructor **CUnknown.**



| Variables de miembro protegido                                                  | Descripción                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m \_ cRef**](cunknown-m-cref.md)                                          | Recuento de referencias.                                                   |
| Métodos públicos                                                              | Descripción                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Método constructor.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Método destructor. Virtual.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Obtiene un puntero al control **IUnknown**.                    |
| Métodos INonDelegatingUnknown                                               | Descripción                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Incrementa el recuento de referencias.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Recupera un puntero de interfaz e incrementa el recuento de referencias. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Disminuye el recuento de referencias.                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 




