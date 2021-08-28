---
description: La interfaz INonDelegatingUnknown es una versión de IUnknown cuyo nombre se ha cambiado para habilitar la compatibilidad con interfaces IUnknown no delegando y delegando en el mismo objeto COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (Combase.h)
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
ms.openlocfilehash: f733ba28af1b4ecb7fc0a52852b4d8663fddf1df07572c409136a9aa963ba076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051615"
---
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

La interfaz es una versión de IUnknown cuyo nombre se ha cambiado para habilitar la compatibilidad con las `INonDelegatingUnknown` interfaces **IUnknown** no delegando y delegando en el mismo objeto COM. 

## <a name="syntax"></a>Sintaxis


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Comentarios

Para usar `INonDelegatingUnknown` para la herencia múltiple, realice los pasos siguientes.

1.  Derive la clase de una interfaz, por ejemplo, IMyInterface.
2.  Incluya [**DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la definición de clase para declarar implementaciones de **QueryInterface,** **AddRef** y **Release** que llaman al desconocido externo.
3.  Invalide **NonDelegatingQueryInterface para** exponer IMyInterface con código como el siguiente:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Declare e implemente las funciones miembro de IMyInterface.

Para usar `INonDelegatingUnknown` para interfaces anidadas, realice los pasos siguientes:

1.  Declare una clase derivada de [**CUnknown**](cunknown.md).
2.  Incluya [**DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la definición de clase.
3.  Invalide **NonDelegatingQueryInterface para** exponer IMyInterface con el código como el siguiente:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implemente las funciones miembro de IMyInterface. Use [**CUnknown::GetOwner para**](cunknown-getowner.md) tener acceso a la clase de objeto COM.
5.  En la clase de objeto COM, haga que la clase anidada sea un amigo de la clase de objeto COM y declare una instancia de la clase anidada como miembro de la clase de objeto COM.

Dado que siempre debe pasar el elemento desconocido externo y **un HRESULT** al constructor [**CUnknown,**](cunknown.md) no puede usar un constructor predeterminado. Tiene que convertir la variable miembro en un puntero a la clase y realizar una nueva llamada en el constructor para crearla realmente.

Invalide **NonDelegatingQueryInterface** con código como el siguiente:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Puede tener clases mixtas que admitan algunas interfaces a través de la herencia múltiple y algunas interfaces a través de clases anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 




