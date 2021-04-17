---
description: 'Más información acerca de: JET_SESID. Método ToString (String, IFormatProvider)'
title: JET_SESID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512468
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5565e67cc0f91fd1c2edb0d9c0aa421211c57c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659796"
---
# <a name="jet_sesidtostring-method-string-iformatprovider"></a><span data-ttu-id="715b4-103">JET_SESID. Método ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="715b4-103">JET_SESID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="715b4-104">Da formato al valor de la instancia actual usando el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="715b4-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="715b4-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="715b4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="715b4-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="715b4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="715b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="715b4-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_SESID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="715b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="715b4-108">Parameters</span></span>

  - <span data-ttu-id="715b4-109">format</span><span class="sxs-lookup"><span data-stu-id="715b4-109">format</span></span>  
    <span data-ttu-id="715b4-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="715b4-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="715b4-111">[Cadena](/dotnet/api/system.string) que especifica el formato que se va a utilizar. o bien, null para usar el formato predeterminado definido para el tipo de la implementación de [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="715b4-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="715b4-112">FormatProvider (</span><span class="sxs-lookup"><span data-stu-id="715b4-112">formatProvider</span></span>  
    <span data-ttu-id="715b4-113">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="715b4-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="715b4-114">[IFormatProvider](/dotnet/api/system.iformatprovider) que se va a utilizar para dar formato al valor; o bien, null para obtener la información de formato numérico de la configuración regional actual del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="715b4-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="715b4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="715b4-115">Return value</span></span>

<span data-ttu-id="715b4-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="715b4-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="715b4-117">[Cadena](/dotnet/api/system.string) que contiene el valor de la instancia actual en el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="715b4-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="715b4-118">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="715b4-118">Implements</span></span>

[<span data-ttu-id="715b4-119">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="715b4-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="715b4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="715b4-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="715b4-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="715b4-121">Reference</span></span>

[<span data-ttu-id="715b4-122">Estructura de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="715b4-122">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="715b4-123">Miembros de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="715b4-123">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="715b4-124">Sobrecarga de ToString</span><span class="sxs-lookup"><span data-stu-id="715b4-124">ToString overload</span></span>](./jet-sesid.tostring-method2.md)

[<span data-ttu-id="715b4-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="715b4-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
