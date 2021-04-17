---
title: Conversión
description: Lo utiliza el cuadro de diálogo convertir para determinar los formatos que una aplicación puede leer y escribir.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Clave del registro de conversión COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532457"
---
# <a name="conversion"></a><span data-ttu-id="ac20b-104">Conversión</span><span class="sxs-lookup"><span data-stu-id="ac20b-104">Conversion</span></span>

<span data-ttu-id="ac20b-105">Lo utiliza el cuadro de diálogo **convertir** para determinar los formatos que una aplicación puede leer y escribir.</span><span class="sxs-lookup"><span data-stu-id="ac20b-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ac20b-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="ac20b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="ac20b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac20b-107">Remarks</span></span>

<span data-ttu-id="ac20b-108">La información de conversión se usa en el cuadro de diálogo **convertir** para determinar qué formatos puede leer y escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac20b-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="ac20b-109">Un formato de archivo delimitado por comas se indica mediante un número si es uno de los formatos del portapapeles definido en Windows. h.</span><span class="sxs-lookup"><span data-stu-id="ac20b-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="ac20b-110">Una cadena indica que el formato no es uno definido en Windows. h (privado).</span><span class="sxs-lookup"><span data-stu-id="ac20b-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="ac20b-111">En este caso, el formato legible y grabable es CF \_ Outline (Private).</span><span class="sxs-lookup"><span data-stu-id="ac20b-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="ac20b-112">El valor *rformat* especifica el formato de archivo que una aplicación puede leer (convertir de).</span><span class="sxs-lookup"><span data-stu-id="ac20b-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="ac20b-113">El valor *rwformat* especifica el formato de archivo que una aplicación puede leer y escribir (activar como).</span><span class="sxs-lookup"><span data-stu-id="ac20b-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




