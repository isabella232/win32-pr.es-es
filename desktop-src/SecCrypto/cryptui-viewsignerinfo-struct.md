---
description: Contiene información de la función CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Estructura de CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082642"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="de0b8-103">\_VIEWSIGNERINFO \_ estructura de estructura CRYPTUI</span><span class="sxs-lookup"><span data-stu-id="de0b8-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="de0b8-104">\[La estructura de **\_ \_ struct de CRYPTUI VIEWSIGNERINFO** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="de0b8-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="de0b8-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="de0b8-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="de0b8-106">La estructura de estructura **CRYPTUI \_ \_ VIEWSIGNERINFO** contiene información para la función [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="de0b8-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="de0b8-107">Esta estructura no se declara en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="de0b8-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="de0b8-108">Para usar esta estructura, declárela en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="de0b8-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="de0b8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de0b8-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="de0b8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="de0b8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="de0b8-111">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="de0b8-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-112">Tamaño, en bytes, de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="de0b8-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-113">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="de0b8-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-114">Identificador de la ventana que va a ser el elemento primario del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="de0b8-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="de0b8-115">Este miembro puede ser **null** si el cuadro de diálogo no debe tener ningún elemento primario.</span><span class="sxs-lookup"><span data-stu-id="de0b8-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="de0b8-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-117">Un conjunto de marcas que modifica el comportamiento de la función [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="de0b8-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="de0b8-118">No hay marcas definidas actualmente, por lo que este miembro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="de0b8-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-119">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="de0b8-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-120">Puntero a una cadena terminada en null que contiene el título que se va a mostrar en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="de0b8-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="de0b8-121">Si este miembro es **null**, se utiliza un título predeterminado.</span><span class="sxs-lookup"><span data-stu-id="de0b8-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-122">**pSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="de0b8-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-123">Un puntero a una estructura de [**\_ \_ información del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) que contiene la información del firmante que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="de0b8-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-124">**hMsg**</span><span class="sxs-lookup"><span data-stu-id="de0b8-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-125">Identificador del mensaje del que se extrajo la información del firmante.</span><span class="sxs-lookup"><span data-stu-id="de0b8-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-126">**pszOID**</span><span class="sxs-lookup"><span data-stu-id="de0b8-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-127">Puntero a una cadena ANSI terminada en null que contiene la representación de cadena del [*identificador de objeto*](../secgloss/o-gly.md) (OID) que indica el certificado para el que se debe validar la firma.</span><span class="sxs-lookup"><span data-stu-id="de0b8-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="de0b8-128">Por ejemplo, si se llama a este método para ver la firma de una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL), se debe pasar la cadena de OID de **firma de uso de szOID \_ PK \_ CTL \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="de0b8-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="de0b8-129">Si este miembro es **null**, el certificado no se valida para los usos.</span><span class="sxs-lookup"><span data-stu-id="de0b8-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-130">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="de0b8-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-131">Este parámetro no se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="de0b8-131">This parameter is not currently used.</span></span> <span data-ttu-id="de0b8-132">Este miembro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="de0b8-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-133">**cStores**</span><span class="sxs-lookup"><span data-stu-id="de0b8-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-134">Número de elementos de la matriz **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="de0b8-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-135">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="de0b8-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-136">Matriz de valores **HCERTSTORE** que representan los otros almacenes de certificados en los que se va a buscar el certificado que firmó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="de0b8-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="de0b8-137">Si este miembro es **null**, no se busca ningún almacén adicional.</span><span class="sxs-lookup"><span data-stu-id="de0b8-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="de0b8-138">El miembro **cStores** contiene el número de elementos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="de0b8-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-139">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="de0b8-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-140">Número de elementos de la matriz **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="de0b8-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="de0b8-141">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="de0b8-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="de0b8-142">Matriz de punteros de estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) que definen las páginas adicionales que se van a mostrar en el cuadro de diálogo estándar.</span><span class="sxs-lookup"><span data-stu-id="de0b8-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="de0b8-143">Si este miembro es **null**, no se mostrará ninguna página adicional.</span><span class="sxs-lookup"><span data-stu-id="de0b8-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="de0b8-144">El miembro **cPropSheetPages** contiene el número de elementos de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="de0b8-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de0b8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de0b8-145">Requirements</span></span>



| <span data-ttu-id="de0b8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="de0b8-146">Requirement</span></span> | <span data-ttu-id="de0b8-147">Value</span><span class="sxs-lookup"><span data-stu-id="de0b8-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de0b8-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de0b8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="de0b8-149">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="de0b8-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="de0b8-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de0b8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="de0b8-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="de0b8-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de0b8-152">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="de0b8-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="de0b8-153">**CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) y **CRYPTUI \_ VIEWSIGNERINFO \_ Structa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="de0b8-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de0b8-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="de0b8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0b8-155">**CryptUIDlgViewSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="de0b8-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
