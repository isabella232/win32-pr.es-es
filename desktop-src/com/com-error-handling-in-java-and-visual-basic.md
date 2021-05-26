---
title: Control de errores COM en Java y Visual Basic
description: Control de errores COM en Java y Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424015"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="b8afd-103">Control de errores COM en Java y Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b8afd-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="b8afd-104">Hay tres interfaces y tres funciones que se pueden usar en COM para proporcionar control de errores al programar en Java o Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b8afd-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="b8afd-105">En Java y Visual Basic, la llamada al método no devuelve **un valor HRESULT** como valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b8afd-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="b8afd-106">En su lugar, estos lenguajes usan las interfaces y funciones COM para obtener valores **HRESULT** y controlar errores o excepciones.</span><span class="sxs-lookup"><span data-stu-id="b8afd-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="b8afd-107">(Las excepciones son eventos más allá del control del programa, como problemas de archivo o parámetros no válidos).</span><span class="sxs-lookup"><span data-stu-id="b8afd-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="b8afd-108">Las tres interfaces que proporcionan compatibilidad con **HRESULT** se enumeran y describen brevemente en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b8afd-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|  <span data-ttu-id="b8afd-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b8afd-109">Interface</span></span>                                                                        |  <span data-ttu-id="b8afd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8afd-110">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8afd-111">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b8afd-111">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="b8afd-112">Establece la información de error.</span><span class="sxs-lookup"><span data-stu-id="b8afd-112">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="b8afd-113">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b8afd-113">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="b8afd-114">Devuelve información de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="b8afd-114">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="b8afd-115">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b8afd-115">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="b8afd-116">Identifica el objeto como compatible con la [**interfaz IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)</span><span class="sxs-lookup"><span data-stu-id="b8afd-116">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="b8afd-117">Las tres funciones que proporcionan compatibilidad con **HRESULT** se enumeran y describen brevemente en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b8afd-117">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|    <span data-ttu-id="b8afd-118">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b8afd-118">Interface</span></span>       |       <span data-ttu-id="b8afd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8afd-119">Description</span></span>       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8afd-120">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b8afd-120">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="b8afd-121">Crea una instancia de un objeto de error genérico.</span><span class="sxs-lookup"><span data-stu-id="b8afd-121">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="b8afd-122">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b8afd-122">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="b8afd-123">Obtiene el puntero de información de error establecido por la llamada anterior a [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) en el subproceso lógico actual.</span><span class="sxs-lookup"><span data-stu-id="b8afd-123">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="b8afd-124">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b8afd-124">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="b8afd-125">Establece el objeto de información de error para el subproceso actual de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b8afd-125">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b8afd-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8afd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8afd-127">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="b8afd-127">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

