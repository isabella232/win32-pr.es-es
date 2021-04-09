---
title: WM/EncodingTime
description: El atributo WM/EncodingTime contiene una marca de tiempo de la hora a la que se ha codificado el contenido.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato de Windows Media WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076937"
---
# <a name="wmencodingtime"></a><span data-ttu-id="ea27b-104">WM/EncodingTime</span><span class="sxs-lookup"><span data-stu-id="ea27b-104">WM/EncodingTime</span></span>

<span data-ttu-id="ea27b-105">El atributo **WM/EncodingTime** contiene una marca de tiempo de la hora a la que se ha codificado el contenido.</span><span class="sxs-lookup"><span data-stu-id="ea27b-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ea27b-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="ea27b-106">Global Constant</span></span>

<span data-ttu-id="ea27b-107">g \_ wszWMEncodingTime</span><span class="sxs-lookup"><span data-stu-id="ea27b-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="ea27b-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ea27b-108">Data Type</span></span>

<span data-ttu-id="ea27b-109">**FILETIME** (**\_ tipo WMT \_ QWord**)</span><span class="sxs-lookup"><span data-stu-id="ea27b-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="ea27b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea27b-110">Remarks</span></span>

<span data-ttu-id="ea27b-111">Este atributo usa un valor de FILETIME, que es un valor de 64 bits que representa el número de unidades de tiempo de 100-nanosegundos transcurridos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="ea27b-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="ea27b-112">Para obtener más información acerca de FILETIME, consulte la sección información del sistema de Windows del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="ea27b-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="ea27b-113">No es un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="ea27b-113">This is not a coded attribute.</span></span> <span data-ttu-id="ea27b-114">Debe establecerlo manualmente si desea incluirlo en los archivos.</span><span class="sxs-lookup"><span data-stu-id="ea27b-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea27b-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea27b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea27b-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="ea27b-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




