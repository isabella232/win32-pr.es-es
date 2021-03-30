---
description: Función de devolución de llamada definida por el usuario que permite al llamador de la función CryptUIDlgSelectCertificate controlar la presentación de los certificados que el usuario selecciona para su visualización.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Función de devolución de llamada PFNCCERTDISPLAYPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082709"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="30e5e-103">Función de devolución de llamada PFNCCERTDISPLAYPROC</span><span class="sxs-lookup"><span data-stu-id="30e5e-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="30e5e-104">La función **PFNCCERTDISPLAYPROC** es una función de devolución de llamada definida por el usuario que permite al autor de la llamada de la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) controlar la presentación de los certificados que el usuario selecciona para verlos.</span><span class="sxs-lookup"><span data-stu-id="30e5e-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30e5e-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="30e5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30e5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e5e-107">*pCertContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30e5e-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30e5e-108">Puntero a una estructura [**de \_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="30e5e-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="30e5e-109">*hWndSelCertDlg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30e5e-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30e5e-110">Identificador del cuadro de diálogo del que se seleccionó el certificado para su visualización.</span><span class="sxs-lookup"><span data-stu-id="30e5e-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="30e5e-111">*pvCallbackData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30e5e-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30e5e-112">Datos adicionales usados por la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="30e5e-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e5e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30e5e-113">Return value</span></span>

<span data-ttu-id="30e5e-114">Esta función devuelve **true** para indicar que controla la presentación del certificado y que el cuadro de diálogo no debe mostrar el certificado.</span><span class="sxs-lookup"><span data-stu-id="30e5e-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="30e5e-115">Si esta función devuelve **false**, el cuadro de diálogo muestra el certificado.</span><span class="sxs-lookup"><span data-stu-id="30e5e-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e5e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30e5e-116">Requirements</span></span>



| <span data-ttu-id="30e5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e5e-117">Requirement</span></span> | <span data-ttu-id="30e5e-118">Value</span><span class="sxs-lookup"><span data-stu-id="30e5e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30e5e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30e5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30e5e-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="30e5e-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="30e5e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30e5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30e5e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30e5e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




