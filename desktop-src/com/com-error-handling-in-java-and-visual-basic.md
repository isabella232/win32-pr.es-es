---
title: Control de errores COM en Java y Visual Basic
description: Control de errores COM en Java y Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421463"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="11438-103">Control de errores COM en Java y Visual Basic</span><span class="sxs-lookup"><span data-stu-id="11438-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="11438-104">Hay tres interfaces y tres funciones que se pueden usar en COM para proporcionar control de errores al programar en Java o Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11438-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="11438-105">En Java y Visual Basic, la llamada al método no devuelve un **HRESULT** como el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="11438-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="11438-106">En su lugar, estos lenguajes utilizan las interfaces y funciones COM para obtener los valores **HRESULT** y controlar los errores o excepciones.</span><span class="sxs-lookup"><span data-stu-id="11438-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="11438-107">(Las excepciones son eventos más allá del control del programa, como problemas de archivos o parámetros no válidos).</span><span class="sxs-lookup"><span data-stu-id="11438-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="11438-108">Las tres interfaces que proporcionan compatibilidad con **HRESULT** s se enumeran y describen brevemente en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="11438-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11438-109">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="11438-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="11438-110">Establece la información de error.</span><span class="sxs-lookup"><span data-stu-id="11438-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="11438-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="11438-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="11438-112">Devuelve información de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="11438-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="11438-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="11438-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="11438-114">Identifica el objeto como compatible con la interfaz [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="11438-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="11438-115">Las tres funciones que proporcionan compatibilidad con **HRESULT** s se enumeran y describen brevemente en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="11438-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11438-116">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="11438-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="11438-117">Crea una instancia de un objeto de error genérico.</span><span class="sxs-lookup"><span data-stu-id="11438-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="11438-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="11438-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="11438-119">Obtiene el puntero de información de error establecido por la llamada anterior a [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) en el subproceso lógico actual.</span><span class="sxs-lookup"><span data-stu-id="11438-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="11438-120">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="11438-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="11438-121">Establece el objeto de información de error para el subproceso de ejecución actual.</span><span class="sxs-lookup"><span data-stu-id="11438-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="11438-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11438-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11438-123">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="11438-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

