---
description: Contiene información sobre el cuadro de diálogo que muestra la función CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Estructura de CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669738"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="55148-103">\_SELECTCERTIFICATE \_ estructura de estructura CRYPTUI</span><span class="sxs-lookup"><span data-stu-id="55148-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="55148-104">La estructura de estructura **CRYPTUI \_ \_ SELECTCERTIFICATE** contiene información sobre el cuadro de diálogo que muestra la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="55148-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="55148-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55148-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="55148-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="55148-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="55148-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="55148-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="55148-108">Tamaño, en bytes, de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="55148-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="55148-109">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="55148-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="55148-110">Identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55148-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="55148-111">Si este valor es **null**, la ventana primaria es la ventana de escritorio predeterminada.</span><span class="sxs-lookup"><span data-stu-id="55148-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="55148-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="55148-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="55148-113">Especifica opciones adicionales para la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="55148-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="55148-114">Puede ser cero o **una operación OR bit a bit** de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="55148-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="55148-115">Value</span><span class="sxs-lookup"><span data-stu-id="55148-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="55148-116">Significado</span><span class="sxs-lookup"><span data-stu-id="55148-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="55148-117"><dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt></span><span class="sxs-lookup"><span data-stu-id="55148-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="55148-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="55148-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="55148-119"><dt>**CRYPTUI \_ SELECTCERT \_ heredado**</dt></span><span class="sxs-lookup"><span data-stu-id="55148-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="55148-120">Especifica que se va a mostrar el cuadro de diálogo heredado.</span><span class="sxs-lookup"><span data-stu-id="55148-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="55148-121"><dt>**CRYPTUI \_ SELECTCERT \_ MultiSelect**</dt></span><span class="sxs-lookup"><span data-stu-id="55148-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="55148-122">Permite al usuario seleccionar más de un certificado en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55148-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="55148-123">Si se establece esta marca, la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) siempre devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="55148-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="55148-124">El miembro **hSelectedCertStore** de esta estructura debe contener un identificador para un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="55148-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="55148-125">Los certificados seleccionados por el usuario se agregarán a este almacén.</span><span class="sxs-lookup"><span data-stu-id="55148-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="55148-126"><dt>**\_ \_ \_ \_ nivel superior de la ventana de SELECTCERT de CRYPTUI**</dt></span><span class="sxs-lookup"><span data-stu-id="55148-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="55148-127">Obliga a que la interfaz de usuario de criptografía sea la ventana superior de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="55148-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="55148-128">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="55148-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="55148-129">Título para mostrar del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55148-129">The display title for the dialog box.</span></span> <span data-ttu-id="55148-130">Si el valor de este miembro es **null**, se usa el título predeterminado de "seleccionar certificado".</span><span class="sxs-lookup"><span data-stu-id="55148-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="55148-131">**dwDontUseColumn**</span><span class="sxs-lookup"><span data-stu-id="55148-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="55148-132">Marcas que se pueden combinar para excluir columnas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="55148-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="55148-133">Value</span><span class="sxs-lookup"><span data-stu-id="55148-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="55148-134">Significado</span><span class="sxs-lookup"><span data-stu-id="55148-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="55148-135"><dt>**CRYPTUI \_ SELECT \_ ISSUED to \_ Column**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="55148-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="55148-136">No Mostrar información de **emitido** .</span><span class="sxs-lookup"><span data-stu-id="55148-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="55148-137"><dt>**CRYPTUI \_ SELECCIONAR \_ ISSUEDBY \_ columna**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="55148-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="55148-138">No Mostrar información de **ISSUEDBY** .</span><span class="sxs-lookup"><span data-stu-id="55148-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="55148-139"><dt>**CRYPTUI \_ SELECCIONAR \_ INTENDEDUSE \_ columna**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="55148-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="55148-140">No Mostrar información de **IntendedUse** .</span><span class="sxs-lookup"><span data-stu-id="55148-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="55148-141"><dt>**CRYPTUI \_ SELECCIONAR \_ FRIENDLYNAME \_ columna**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="55148-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="55148-142">No Mostrar información del nombre.</span><span class="sxs-lookup"><span data-stu-id="55148-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="55148-143"><dt>**CRYPTUI \_ SELECCIONAR \_ Ubicación \_ columna**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="55148-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="55148-144">No Mostrar información de ubicación.</span><span class="sxs-lookup"><span data-stu-id="55148-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="55148-145"><dt>**CRYPTUI \_ Seleccionar \_ la \_ columna de expiración**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="55148-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="55148-146">No Mostrar información de expiración.</span><span class="sxs-lookup"><span data-stu-id="55148-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="55148-147">**szDisplayString**</span><span class="sxs-lookup"><span data-stu-id="55148-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="55148-148">Texto que se muestra en el cuadro de diálogo para indicar al usuario.</span><span class="sxs-lookup"><span data-stu-id="55148-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="55148-149">Si el valor de este miembro es **null**, se usa la cadena predeterminada "Seleccione un certificado que desee usar".</span><span class="sxs-lookup"><span data-stu-id="55148-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="55148-150">**pFilterCallback**</span><span class="sxs-lookup"><span data-stu-id="55148-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="55148-151">Puntero a una función de devolución de llamada [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) que filtra los certificados que se muestran en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55148-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="55148-152">**pDisplayCallback**</span><span class="sxs-lookup"><span data-stu-id="55148-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="55148-153">Puntero a una función de devolución de llamada [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) que muestra los certificados que el usuario selecciona para su visualización.</span><span class="sxs-lookup"><span data-stu-id="55148-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="55148-154">**pvCallbackData**</span><span class="sxs-lookup"><span data-stu-id="55148-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="55148-155">Datos adicionales que se pasan a las funciones de devolución de llamada especificadas por los miembros **pFilterCallback** y **pDisplayCallback** .</span><span class="sxs-lookup"><span data-stu-id="55148-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="55148-156">**cDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="55148-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="55148-157">El número de almacenes de certificados en la matriz **rghDisplayStores** .</span><span class="sxs-lookup"><span data-stu-id="55148-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="55148-158">**rghDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="55148-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="55148-159">Puntero a una matriz de almacenes que contienen certificados disponibles para la selección en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55148-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="55148-160">**cStores**</span><span class="sxs-lookup"><span data-stu-id="55148-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="55148-161">El número de almacenes de certificados en la matriz **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="55148-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="55148-162">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="55148-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="55148-163">Puntero a una matriz de almacenes de certificados en los que se va a buscar al compilar una cadena de certificados y comprobar la confianza de los certificados mostrados en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55148-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="55148-164">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="55148-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="55148-165">El número de páginas de propiedades de la matriz **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="55148-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="55148-166">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="55148-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="55148-167">Puntero a una matriz de estructuras **PROPSHEETPAGE** que representan las páginas de propiedades que se pasan al cuadro de diálogo visualización de certificados cuando se selecciona un certificado para su visualización.</span><span class="sxs-lookup"><span data-stu-id="55148-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="55148-168">**hSelectedCertStore**</span><span class="sxs-lookup"><span data-stu-id="55148-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="55148-169">Identificador de un almacén de certificados creado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="55148-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="55148-170">Los certificados seleccionados por el usuario se agregan a este almacén.</span><span class="sxs-lookup"><span data-stu-id="55148-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="55148-171">Si el número de certificados de este almacén es el mismo antes y después de llamar a [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), el usuario ha cerrado el cuadro de diálogo sin seleccionar ningún certificado.</span><span class="sxs-lookup"><span data-stu-id="55148-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="55148-172">Este miembro no se usa si el miembro **dwFlags** de esta estructura no contiene el marcador **de \_ \_ selección MultiSelect CRYPTUI SELECTCERT** .</span><span class="sxs-lookup"><span data-stu-id="55148-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55148-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55148-173">Requirements</span></span>



| <span data-ttu-id="55148-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="55148-174">Requirement</span></span> | <span data-ttu-id="55148-175">Value</span><span class="sxs-lookup"><span data-stu-id="55148-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55148-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55148-176">Minimum supported client</span></span><br/> | <span data-ttu-id="55148-177">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="55148-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="55148-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55148-178">Minimum supported server</span></span><br/> | <span data-ttu-id="55148-179">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="55148-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="55148-180">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="55148-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="55148-181">**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) y **CRYPTUI \_ SELECTCERTIFICATE \_ Structa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="55148-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55148-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="55148-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55148-183">**CryptUIDlgSelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="55148-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




