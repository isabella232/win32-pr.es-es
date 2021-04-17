---
description: La interfaz INonDelegatingUnknown es una versión de IUnknown cuyo nombre se ha cambiado para habilitar la compatibilidad con las interfaces IUnknown no delegar y delegar en el mismo objeto COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680934"
---
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

La `INonDelegatingUnknown` interfaz es una versión de **IUnknown** cuyo nombre se ha cambiado para habilitar la compatibilidad con las interfaces **IUnknown** que no se delegan y que delegan en el mismo objeto com.

## <a name="syntax"></a>Sintaxis


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Observaciones

Para usar `INonDelegatingUnknown` para herencia múltiple, realice los pasos siguientes.

1.  Derive la clase de una interfaz, por ejemplo, IMyInterface.
2.  Incluya [**declare \_ IUNKNOWN**](declare-iunknown.md) en la definición de clase para declarar implementaciones de **QueryInterface**, **AddRef** y **Release** que llamen al desconocido externo.
3.  Invalide **NonDelegatingQueryInterface** para exponer IMyInterface con código como el siguiente:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Declare e implemente las funciones miembro de IMyInterface.

Para usar `INonDelegatingUnknown` para las interfaces anidadas, realice los pasos siguientes:

1.  Declare una clase derivada de [**CUnknown**](cunknown.md).
2.  Incluya [**declare \_ IUNKNOWN**](declare-iunknown.md) en la definición de clase.
3.  Invalide **NonDelegatingQueryInterface** para exponer IMyInterface con el código como el siguiente:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implemente las funciones miembro de IMyInterface. Use [**CUnknown:: GetOwner**](cunknown-getowner.md) para tener acceso a la clase de objeto com.
5.  En la clase de objeto COM, haga que la clase anidada sea Friend de la clase de objeto COM y declare una instancia de la clase anidada como miembro de la clase de objeto COM.

Dado que siempre debe pasar el Unknown externo y un **HRESULT** al constructor [**CUnknown**](cunknown.md) , no puede usar un constructor predeterminado. Tiene que convertir la variable miembro en un puntero a la clase y realizar una nueva llamada en el constructor para crearla realmente.

Invalide **NonDelegatingQueryInterface** con código como el siguiente:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Puede tener clases mixtas que admitan algunas interfaces mediante herencia múltiple y algunas interfaces a través de clases anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones auxiliares de COM**](com-helper-functions.md)
</dt> </dl>

 

 




