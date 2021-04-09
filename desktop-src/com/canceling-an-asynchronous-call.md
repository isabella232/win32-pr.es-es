---
title: Cancelar una llamada asincrónica
description: Un cliente puede cancelar una llamada asincrónica que está en curso si el objeto de llamada implementa la interfaz ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149665"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="14a87-103">Cancelar una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="14a87-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="14a87-104">Un cliente puede cancelar una llamada asincrónica que está en curso si el objeto de llamada implementa la interfaz [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="14a87-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="14a87-105">En el caso de los objetos que usan la serialización estándar, **ICancelMethodCalls** siempre está disponible para las llamadas de serialización.</span><span class="sxs-lookup"><span data-stu-id="14a87-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="14a87-106">En el caso de los objetos que usan el cálculo de referencias personalizado o las llamadas a objetos de servidor dentro del mismo apartamento, esta funcionalidad solo está disponible si el objeto de llamada implementa **ICancelMethodCalls**.</span><span class="sxs-lookup"><span data-stu-id="14a87-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="14a87-107">El cliente puede cancelar la llamada en cualquier momento, desde el momento en \_ que se llama al método Begin hasta que el \_ método Finish vuelve.</span><span class="sxs-lookup"><span data-stu-id="14a87-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="14a87-108">Si el cliente cancela la llamada antes de llamar al \_ método de finalización, debe llamar al \_ método de finalización para limpiar el estado del objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="14a87-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="14a87-109">Hasta que el cliente lo haya hecho, todas las llamadas a cualquier \_ método Begin en el objeto Call devolverán una \_ llamada RPC E \_ \_ Pending.</span><span class="sxs-lookup"><span data-stu-id="14a87-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="14a87-110">**Para cancelar una llamada asincrónica**</span><span class="sxs-lookup"><span data-stu-id="14a87-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="14a87-111">Consulte el objeto de llamada para [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span><span class="sxs-lookup"><span data-stu-id="14a87-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="14a87-112">Llame a [**ICancelMethodCalls:: CANCEL**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)y llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar el puntero que obtiene la llamada [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="14a87-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="14a87-113">Si el cliente ya no ha llamado al método de finalización \_ , llámelo ahora.</span><span class="sxs-lookup"><span data-stu-id="14a87-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="14a87-114">No hay ninguna garantía de que el servidor detuviera realmente la ejecución de la llamada.</span><span class="sxs-lookup"><span data-stu-id="14a87-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="14a87-115">Si el trabajo del cliente depende de algún estado del servidor que la llamada puede haber cambiado o no, el cliente debe determinar ese estado antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="14a87-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14a87-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14a87-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a87-117">Realización de una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="14a87-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 