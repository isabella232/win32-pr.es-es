---
title: Estilos extendidos de control ComboBoxEx (CommCtrl. h)
description: Admite los estilos extendidos que se enumeran en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653594"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="6f7b1-103">Estilos extendidos del control ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="6f7b1-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="6f7b1-104">Admite los estilos extendidos que se enumeran en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="6f7b1-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6f7b1-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="6f7b1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f7b1-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="6f7b1-107"><dt>**CBES \_ ex \_ CASESENSITIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="6f7b1-108">Las búsquedas **BSTR** en la lista distinguirán mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="6f7b1-109">Esto incluye las búsquedas como resultado del texto que se va a escribir en el cuadro de edición y el \_ mensaje CB FindExactString con.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="6f7b1-110"><dt>**CBES \_ ex \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="6f7b1-111">En el cuadro de edición y en la lista desplegable no se mostrarán las imágenes del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="6f7b1-112"><dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="6f7b1-113">En el cuadro de edición y en la lista desplegable no se mostrarán las imágenes del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="6f7b1-114"><dt>**CBES \_ ex \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="6f7b1-115">Permite que el control ComboBoxEx tenga un tamaño vertical menor que el control de cuadro combinado que contiene.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="6f7b1-116">Si el tamaño de ComboBoxEx es menor que el cuadro combinado, el cuadro combinado se recortará.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="6f7b1-117"><dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="6f7b1-118">Solo Windows NT.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-118">Windows NT only.</span></span> <span data-ttu-id="6f7b1-119">El cuadro de edición utilizará la barra diagonal (/), la barra diagonal inversa ( \) y los caracteres de punto (.) como delimitadores de palabras.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-119">The edit box will use the slash (/), backslash (\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="6f7b1-120">Esto hace que los métodos abreviados de teclado para el movimiento de cursor de palabra por palabra funcionen en los nombres de ruta de acceso y las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="6f7b1-121"><dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="6f7b1-122">**Windows Vista y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="6f7b1-122">**Windows Vista and later.**</span></span> <span data-ttu-id="6f7b1-123">Hace que los elementos de la lista desplegable y el cuadro de edición (cuando el cuadro de edición es de solo lectura) se trunquen con puntos suspensivos ("...") en lugar de simplemente recortados por el borde del control.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="6f7b1-124">Esto resulta útil cuando el control debe establecerse en un ancho fijo, pero las entradas de la lista pueden ser largas.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f7b1-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f7b1-125">Remarks</span></span>

<span data-ttu-id="6f7b1-126">Los estilos extendidos de ComboBox se establecen y recuperan mediante los mensajes [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) y [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7b1-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="6f7b1-127">Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo [**\_ simple CBS**](combo-box-styles.md) , es posible que no se vuelva a dibujar correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="6f7b1-128">El **estilo \_ simple CBS** tampoco funciona correctamente con el \_ estilo extendido CBES ex \_ PATHWORDBREAKPROC.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f7b1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f7b1-129">Requirements</span></span>



| <span data-ttu-id="6f7b1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f7b1-130">Requirement</span></span> | <span data-ttu-id="6f7b1-131">Value</span><span class="sxs-lookup"><span data-stu-id="6f7b1-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7b1-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f7b1-132">Header</span></span><br/> | <dl> <span data-ttu-id="6f7b1-133"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b1-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





