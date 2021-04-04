---
title: Control de errores desconocidos
description: Control de errores desconocidos
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076285"
---
# <a name="handling-unknown-errors"></a><span data-ttu-id="aedc2-103">Control de errores desconocidos</span><span class="sxs-lookup"><span data-stu-id="aedc2-103">Handling Unknown Errors</span></span>

<span data-ttu-id="aedc2-104">Es válido devolver un código de estado solo desde la implementación de un método de interfaz autorizada como devuelto legalmente.</span><span class="sxs-lookup"><span data-stu-id="aedc2-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="aedc2-105">Si no se observa esta regla, se invita a la posibilidad de que se produzca un conflicto entre los valores devueltos del código de error y los autorizados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aedc2-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="aedc2-106">Preste especial atención a este posible problema al propagar los códigos de error de las funciones a las que se llama internamente.</span><span class="sxs-lookup"><span data-stu-id="aedc2-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="aedc2-107">Las aplicaciones que llaman a interfaces deben tratar cualquier código de error devuelto desconocido (en lugar de un código correcto) como sinónimo de E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="aedc2-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="aedc2-108">La práctica de controlar códigos de error desconocidos es necesaria para los clientes de las interfaces y funciones definidas por COM.</span><span class="sxs-lookup"><span data-stu-id="aedc2-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="aedc2-109">Dado que la práctica típica de programación consiste en controlar algunos códigos de error específicos en detalle y tratar el resto de forma genérica, se cumple fácilmente este requisito de administrar los códigos de error inesperados o desconocidos.</span><span class="sxs-lookup"><span data-stu-id="aedc2-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="aedc2-110">Es importante controlar todos los posibles errores al llamar a un método de interfaz.</span><span class="sxs-lookup"><span data-stu-id="aedc2-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="aedc2-111">Si no lo hace, la aplicación se bloqueará, se dañarán los datos o se hará vulnerable a las vulnerabilidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="aedc2-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="aedc2-112">En el ejemplo de código siguiente se muestra la forma recomendada de controlar los errores desconocidos:</span><span class="sxs-lookup"><span data-stu-id="aedc2-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



<span data-ttu-id="aedc2-113">La siguiente comprobación de errores suele usarse con esas rutinas que no devuelven nada especial (que no sea \_ correcto o algún error inesperado):</span><span class="sxs-lookup"><span data-stu-id="aedc2-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a><span data-ttu-id="aedc2-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aedc2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aedc2-115">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="aedc2-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




