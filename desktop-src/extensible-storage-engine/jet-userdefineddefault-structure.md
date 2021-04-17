---
description: 'Más información acerca de: estructura de JET_USERDEFINEDDEFAULT'
title: Estructura de JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697674"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="bc3ce-103">Estructura de JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="bc3ce-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="bc3ce-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bc3ce-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="bc3ce-105">Estructura de JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="bc3ce-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="bc3ce-106">La estructura de **JET_USERDEFINEDDEFAULT** se especifica junto con JET_bitColumnUserDefinedDefault para asignar a una nueva columna un valor predeterminado que se determina mediante una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="bc3ce-107">Esta técnica se puede usar para implementar columnas calculadas.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="bc3ce-108">**Windows XP:** La estructura de **JET_USERDEFINEDDEFAULT** se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="bc3ce-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc3ce-109">Members</span></span>

<span data-ttu-id="bc3ce-110">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="bc3ce-110">**szCallback**</span></span>

<span data-ttu-id="bc3ce-111">Nombre de exportación de la función que implementa la devolución de llamada en formato "función de módulo \! ".</span><span class="sxs-lookup"><span data-stu-id="bc3ce-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="bc3ce-112">La devolución de llamada se conserva como parte del esquema de columna.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="bc3ce-113">El ejecutable de host real y el nombre de exportación de la función deben persistir para habilitar la búsqueda de la dirección verdadera de la función en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="bc3ce-114">El nombre del módulo es el nombre del archivo binario del host que contiene la función.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="bc3ce-115">El nombre de la función es el nombre de la exportación para esa función.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="bc3ce-116">El motor de base de datos utilizará estos dos fragmentos de información en tiempo de ejecución para localizar la dirección verdadera de la devolución de llamada mediante la ejecución de una llamada [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) en el nombre del módulo seguido de una llamada [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) en el nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="bc3ce-117">Por ejemplo, si la devolución de llamada se implementó en un archivo DLL denominado MyCallback.DLL y ese archivo DLL se almacenó en C: myFunction \\ y la función que implementa la devolución de llamada se exportó desde el archivo dll como UserDefinedDefaultCallback, la cadena necesaria sería "C: myfunction \\ \\MyCallback.DLL\! UserDefinedDefaultCallback".</span><span class="sxs-lookup"><span data-stu-id="bc3ce-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="bc3ce-118">**Nota:**  Embedded " \! "</span><span class="sxs-lookup"><span data-stu-id="bc3ce-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="bc3ce-119">no se admiten los caracteres de la parte del módulo del nombre de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="bc3ce-120">Se recomienda encarecidamente que use un nombre de devolución de llamada que no sea una función de la arquitectura del host.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="bc3ce-121">Por ejemplo, no utilice exportaciones decoradas como Stdcall ( UserDefinedDefaultCallback@32 ) porque esta Convención de llamada solo se admite en equipos x86.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="bc3ce-122">Si se utilizara esta devolución de llamada, la base de datos solo podría usarse en un equipo x86.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="bc3ce-123">En este caso, se debe usar un alias para realizar una exportación independiente de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="bc3ce-124">Se recomienda encarecidamente que use la ruta de acceso completa del nombre del módulo que implementa la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="bc3ce-125">Si se usa una ruta de acceso relativa, el proceso que hospeda la base de datos puede ser susceptible de sufrir ataques de un archivo binario no autorizado.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="bc3ce-126">La aplicación solo debe pasar devoluciones de llamada de confianza al motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="bc3ce-127">El motor de base de datos cargará el archivo binario para comprobar su existencia cuando se cree la columna asociada.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="bc3ce-128">Si la ruta de acceso al archivo binario no se valida o sabe que es de confianza, podría atacar el proceso que hospeda la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="bc3ce-129">**pbUserData**</span><span class="sxs-lookup"><span data-stu-id="bc3ce-129">**pbUserData**</span></span>

<span data-ttu-id="bc3ce-130">Un bloque independiente de datos definidos por el usuario que se va a pasar a la devolución de llamada cuando se invoca. El bloque de datos que se proporciona se conservará como parte del esquema de columna.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="bc3ce-131">Como resultado, el bloque de datos debe ser completamente independiente y no puede hacer referencia a los datos que están fuera del ámbito de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="bc3ce-132">Si **pbUserData** es cero, se omite el valor de **cbUserData** .</span><span class="sxs-lookup"><span data-stu-id="bc3ce-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="bc3ce-133">En este caso, no se pasarán datos definidos por el usuario a la devolución de llamada cuando se invocan.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="bc3ce-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="bc3ce-134">**cbUserData**</span></span>

<span data-ttu-id="bc3ce-135">Vea **pbUserData**.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-135">See **pbUserData**.</span></span>

<span data-ttu-id="bc3ce-136">**szDependantColumns**</span><span class="sxs-lookup"><span data-stu-id="bc3ce-136">**szDependantColumns**</span></span>

<span data-ttu-id="bc3ce-137">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-137">Reserved for future use.</span></span>

<span data-ttu-id="bc3ce-138">Este miembro siempre debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="bc3ce-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc3ce-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc3ce-140"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bc3ce-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bc3ce-141">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc3ce-142"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bc3ce-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bc3ce-143">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc3ce-144"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bc3ce-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bc3ce-145">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="bc3ce-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc3ce-146"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bc3ce-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bc3ce-147">Se implementa como <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) y <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bc3ce-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bc3ce-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc3ce-148">See Also</span></span>

[<span data-ttu-id="bc3ce-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="bc3ce-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="bc3ce-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="bc3ce-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="bc3ce-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="bc3ce-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
