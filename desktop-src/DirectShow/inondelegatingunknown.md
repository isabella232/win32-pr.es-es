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
# <a name="inondelegatingunknown"></a><span data-ttu-id="be7e7-103">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="be7e7-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="be7e7-104">La `INonDelegatingUnknown` interfaz es una versión de **IUnknown** cuyo nombre se ha cambiado para habilitar la compatibilidad con las interfaces **IUnknown** que no se delegan y que delegan en el mismo objeto com.</span><span class="sxs-lookup"><span data-stu-id="be7e7-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be7e7-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="be7e7-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be7e7-106">Remarks</span></span>

<span data-ttu-id="be7e7-107">Para usar `INonDelegatingUnknown` para herencia múltiple, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="be7e7-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="be7e7-108">Derive la clase de una interfaz, por ejemplo, IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="be7e7-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="be7e7-109">Incluya [**declare \_ IUNKNOWN**](declare-iunknown.md) en la definición de clase para declarar implementaciones de **QueryInterface**, **AddRef** y **Release** que llamen al desconocido externo.</span><span class="sxs-lookup"><span data-stu-id="be7e7-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="be7e7-110">Invalide **NonDelegatingQueryInterface** para exponer IMyInterface con código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="be7e7-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="be7e7-111">Declare e implemente las funciones miembro de IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="be7e7-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="be7e7-112">Para usar `INonDelegatingUnknown` para las interfaces anidadas, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="be7e7-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="be7e7-113">Declare una clase derivada de [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="be7e7-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="be7e7-114">Incluya [**declare \_ IUNKNOWN**](declare-iunknown.md) en la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="be7e7-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="be7e7-115">Invalide **NonDelegatingQueryInterface** para exponer IMyInterface con el código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="be7e7-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="be7e7-116">Implemente las funciones miembro de IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="be7e7-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="be7e7-117">Use [**CUnknown:: GetOwner**](cunknown-getowner.md) para tener acceso a la clase de objeto com.</span><span class="sxs-lookup"><span data-stu-id="be7e7-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="be7e7-118">En la clase de objeto COM, haga que la clase anidada sea Friend de la clase de objeto COM y declare una instancia de la clase anidada como miembro de la clase de objeto COM.</span><span class="sxs-lookup"><span data-stu-id="be7e7-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="be7e7-119">Dado que siempre debe pasar el Unknown externo y un **HRESULT** al constructor [**CUnknown**](cunknown.md) , no puede usar un constructor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="be7e7-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="be7e7-120">Tiene que convertir la variable miembro en un puntero a la clase y realizar una nueva llamada en el constructor para crearla realmente.</span><span class="sxs-lookup"><span data-stu-id="be7e7-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="be7e7-121">Invalide **NonDelegatingQueryInterface** con código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="be7e7-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="be7e7-122">Puede tener clases mixtas que admitan algunas interfaces mediante herencia múltiple y algunas interfaces a través de clases anidadas.</span><span class="sxs-lookup"><span data-stu-id="be7e7-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7e7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7e7-123">Requirements</span></span>



| <span data-ttu-id="be7e7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7e7-124">Requirement</span></span> | <span data-ttu-id="be7e7-125">Value</span><span class="sxs-lookup"><span data-stu-id="be7e7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7e7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be7e7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="be7e7-127"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be7e7-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be7e7-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be7e7-128">Library</span></span><br/> | <dl> <span data-ttu-id="be7e7-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="be7e7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7e7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="be7e7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7e7-131">**Funciones auxiliares de COM**</span><span class="sxs-lookup"><span data-stu-id="be7e7-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




