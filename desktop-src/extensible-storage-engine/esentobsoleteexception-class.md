---
description: 'Más información sobre: clase EsentObsoleteException'
title: Clase EsentObsoleteException
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547275"
---
# <a name="esentobsoleteexception-class"></a><span data-ttu-id="21f62-103">Clase EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="21f62-103">EsentObsoleteException class</span></span>

<span data-ttu-id="21f62-104">Clase base para las excepciones obsoletas.</span><span class="sxs-lookup"><span data-stu-id="21f62-104">Base class for Obsolete exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="21f62-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="21f62-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="21f62-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="21f62-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="21f62-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="21f62-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="21f62-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="21f62-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="21f62-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="21f62-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="21f62-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="21f62-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="21f62-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="21f62-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            

<span data-ttu-id="21f62-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21f62-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21f62-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21f62-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21f62-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21f62-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="21f62-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="21f62-115">Thread safety</span></span>

<span data-ttu-id="21f62-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="21f62-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="21f62-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="21f62-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="21f62-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="21f62-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21f62-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="21f62-119">Reference</span></span>

[<span data-ttu-id="21f62-120">Miembros de EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="21f62-120">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="21f62-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="21f62-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="21f62-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="21f62-122">Derived types</span></span>

[<span data-ttu-id="21f62-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="21f62-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="21f62-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="21f62-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="21f62-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="21f62-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="21f62-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="21f62-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="21f62-127">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="21f62-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="21f62-128">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="21f62-128">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            [<span data-ttu-id="21f62-129">Microsoft. ISAM. esent. Interop. EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="21f62-129">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>](./esentaccessdeniedexception-class.md)  
            [<span data-ttu-id="21f62-130">Microsoft. ISAM. esent. Interop. EsentBadBackupDatabaseSizeException</span><span class="sxs-lookup"><span data-stu-id="21f62-130">Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException</span></span>](./esentbadbackupdatabasesizeexception-class.md)  
            [<span data-ttu-id="21f62-131">Microsoft. ISAM. esent. Interop. EsentBadBookmarkException</span><span class="sxs-lookup"><span data-stu-id="21f62-131">Microsoft.Isam.Esent.Interop.EsentBadBookmarkException</span></span>](./esentbadbookmarkexception-class.md)  
            [<span data-ttu-id="21f62-132">Microsoft. ISAM. esent. Interop. EsentBadDbSignatureException</span><span class="sxs-lookup"><span data-stu-id="21f62-132">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>](./esentbaddbsignatureexception-class.md)  
            [<span data-ttu-id="21f62-133">Microsoft. ISAM. esent. Interop. EsentBadPatchPageException</span><span class="sxs-lookup"><span data-stu-id="21f62-133">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>](./esentbadpatchpageexception-class.md)  
            [<span data-ttu-id="21f62-134">Microsoft. ISAM. esent. Interop. EsentBadSLVSignatureException</span><span class="sxs-lookup"><span data-stu-id="21f62-134">Microsoft.Isam.Esent.Interop.EsentBadSLVSignatureException</span></span>](./esentbadslvsignatureexception-class.md)  
            [<span data-ttu-id="21f62-135">Microsoft. ISAM. esent. Interop. EsentCannotAddFixedVarColumnToDerivedTableException</span><span class="sxs-lookup"><span data-stu-id="21f62-135">Microsoft.Isam.Esent.Interop.EsentCannotAddFixedVarColumnToDerivedTableException</span></span>](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [<span data-ttu-id="21f62-136">Microsoft. ISAM. esent. Interop. EsentCannotNestDistributedTransactionsException</span><span class="sxs-lookup"><span data-stu-id="21f62-136">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>](./esentcannotnestdistributedtransactionsexception-class.md)  
            [<span data-ttu-id="21f62-137">Microsoft. ISAM. esent. Interop. EsentColumnIndexedException</span><span class="sxs-lookup"><span data-stu-id="21f62-137">Microsoft.Isam.Esent.Interop.EsentColumnIndexedException</span></span>](./esentcolumnindexedexception-class.md)  
            [<span data-ttu-id="21f62-138">Microsoft. ISAM. esent. Interop. EsentColumnInRelationshipException</span><span class="sxs-lookup"><span data-stu-id="21f62-138">Microsoft.Isam.Esent.Interop.EsentColumnInRelationshipException</span></span>](./esentcolumninrelationshipexception-class.md)  
            [<span data-ttu-id="21f62-139">Microsoft. ISAM. esent. Interop. EsentColumnLongException</span><span class="sxs-lookup"><span data-stu-id="21f62-139">Microsoft.Isam.Esent.Interop.EsentColumnLongException</span></span>](./esentcolumnlongexception-class.md)  
            [<span data-ttu-id="21f62-140">Microsoft. ISAM. esent. Interop. EsentContainerNotEmptyException</span><span class="sxs-lookup"><span data-stu-id="21f62-140">Microsoft.Isam.Esent.Interop.EsentContainerNotEmptyException</span></span>](./esentcontainernotemptyexception-class.md)  
            [<span data-ttu-id="21f62-141">Microsoft. ISAM. esent. Interop. EsentCurrencyStackOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="21f62-141">Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException</span></span>](./esentcurrencystackoutofmemoryexception-class.md)  
            [<span data-ttu-id="21f62-142">Microsoft. ISAM. esent. Interop. EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="21f62-142">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>](./esentdatabase200formatexception-class.md)  
            [<span data-ttu-id="21f62-143">Microsoft. ISAM. esent. Interop. EsentDatabase400FormatException</span><span class="sxs-lookup"><span data-stu-id="21f62-143">Microsoft.Isam.Esent.Interop.EsentDatabase400FormatException</span></span>](./esentdatabase400formatexception-class.md)  
            [<span data-ttu-id="21f62-144">Microsoft. ISAM. esent. Interop. EsentDatabase500FormatException</span><span class="sxs-lookup"><span data-stu-id="21f62-144">Microsoft.Isam.Esent.Interop.EsentDatabase500FormatException</span></span>](./esentdatabase500formatexception-class.md)  
            [<span data-ttu-id="21f62-145">Microsoft. ISAM. esent. Interop. EsentDatabaseIdInUseException</span><span class="sxs-lookup"><span data-stu-id="21f62-145">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>](./esentdatabaseidinuseexception-class.md)  
            [<span data-ttu-id="21f62-146">Microsoft. ISAM. esent. Interop. EsentDatabasePatchFileMismatchException</span><span class="sxs-lookup"><span data-stu-id="21f62-146">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>](./esentdatabasepatchfilemismatchexception-class.md)  
            [<span data-ttu-id="21f62-147">Microsoft. ISAM. esent. Interop. EsentDatabasesNotFromSameSnapshotException</span><span class="sxs-lookup"><span data-stu-id="21f62-147">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [<span data-ttu-id="21f62-148">Microsoft. ISAM. esent. Interop. EsentDatabaseStreamingFileMismatchException</span><span class="sxs-lookup"><span data-stu-id="21f62-148">Microsoft.Isam.Esent.Interop.EsentDatabaseStreamingFileMismatchException</span></span>](./esentdatabasestreamingfilemismatchexception-class.md)  
            [<span data-ttu-id="21f62-149">Microsoft. ISAM. esent. Interop. EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="21f62-149">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>](./esentdatabaseunavailableexception-class.md)  
            [<span data-ttu-id="21f62-150">Microsoft. ISAM. esent. Interop. EsentDataHasChangedException</span><span class="sxs-lookup"><span data-stu-id="21f62-150">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>](./esentdatahaschangedexception-class.md)  
            [<span data-ttu-id="21f62-151">Microsoft. ISAM. esent. Interop. EsentDistributedTransactionAlreadyPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="21f62-151">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [<span data-ttu-id="21f62-152">Microsoft. ISAM. esent. Interop. EsentDistributedTransactionNotYetPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="21f62-152">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [<span data-ttu-id="21f62-153">Microsoft. ISAM. esent. Interop. EsentDTCCallbackUnexpectedErrorException</span><span class="sxs-lookup"><span data-stu-id="21f62-153">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>](./esentdtccallbackunexpectederrorexception-class.md)  
            [<span data-ttu-id="21f62-154">Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="21f62-154">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>](./esentdtcmissingcallbackexception-class.md)  
            [<span data-ttu-id="21f62-155">Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackOnRecoveryException</span><span class="sxs-lookup"><span data-stu-id="21f62-155">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException</span></span>](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [<span data-ttu-id="21f62-156">Microsoft. ISAM. esent. Interop. EsentFileCloseException</span><span class="sxs-lookup"><span data-stu-id="21f62-156">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>](./esentfilecloseexception-class.md)  
            [<span data-ttu-id="21f62-157">Microsoft. ISAM. esent. Interop. EsentFileIOAbortException</span><span class="sxs-lookup"><span data-stu-id="21f62-157">Microsoft.Isam.Esent.Interop.EsentFileIOAbortException</span></span>](./esentfileioabortexception-class.md)  
            [<span data-ttu-id="21f62-158">Microsoft. ISAM. esent. Interop. EsentFileIOFailException</span><span class="sxs-lookup"><span data-stu-id="21f62-158">Microsoft.Isam.Esent.Interop.EsentFileIOFailException</span></span>](./esentfileiofailexception-class.md)  
            [<span data-ttu-id="21f62-159">Microsoft. ISAM. esent. Interop. EsentFileIORetryException</span><span class="sxs-lookup"><span data-stu-id="21f62-159">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>](./esentfileioretryexception-class.md)  
            [<span data-ttu-id="21f62-160">Microsoft. ISAM. esent. Interop. EsentFileIOSparseException</span><span class="sxs-lookup"><span data-stu-id="21f62-160">Microsoft.Isam.Esent.Interop.EsentFileIOSparseException</span></span>](./esentfileiosparseexception-class.md)  
            [<span data-ttu-id="21f62-161">Microsoft. ISAM. esent. Interop. EsentIndexCantBuildException</span><span class="sxs-lookup"><span data-stu-id="21f62-161">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>](./esentindexcantbuildexception-class.md)  
            [<span data-ttu-id="21f62-162">Microsoft. ISAM. esent. Interop. EsentIndexTuplesTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="21f62-162">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTooManyColumnsException</span></span>](./esentindextuplestoomanycolumnsexception-class.md)  
            [<span data-ttu-id="21f62-163">Microsoft. ISAM. esent. Interop. EsentInvalidCountryException</span><span class="sxs-lookup"><span data-stu-id="21f62-163">Microsoft.Isam.Esent.Interop.EsentInvalidCountryException</span></span>](./esentinvalidcountryexception-class.md)  
            [<span data-ttu-id="21f62-164">Microsoft. ISAM. esent. Interop. EsentInvalidFilenameException</span><span class="sxs-lookup"><span data-stu-id="21f62-164">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>](./esentinvalidfilenameexception-class.md)  
            [<span data-ttu-id="21f62-165">Microsoft. ISAM. esent. Interop. EsentInvalidLogDirectoryException</span><span class="sxs-lookup"><span data-stu-id="21f62-165">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>](./esentinvalidlogdirectoryexception-class.md)  
            [<span data-ttu-id="21f62-166">Microsoft. ISAM. esent. Interop. EsentInvalidLoggedOperationException</span><span class="sxs-lookup"><span data-stu-id="21f62-166">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>](./esentinvalidloggedoperationexception-class.md)  
            [<span data-ttu-id="21f62-167">Microsoft. ISAM. esent. Interop. EsentInvalidObjectException</span><span class="sxs-lookup"><span data-stu-id="21f62-167">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>](./esentinvalidobjectexception-class.md)  
            [<span data-ttu-id="21f62-168">Microsoft. ISAM. esent. Interop. EsentInvalidOnSortException</span><span class="sxs-lookup"><span data-stu-id="21f62-168">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>](./esentinvalidonsortexception-class.md)  
            [<span data-ttu-id="21f62-169">Microsoft. ISAM. esent. Interop. EsentInvalidSystemPathException</span><span class="sxs-lookup"><span data-stu-id="21f62-169">Microsoft.Isam.Esent.Interop.EsentInvalidSystemPathException</span></span>](./esentinvalidsystempathexception-class.md)  
            [<span data-ttu-id="21f62-170">Microsoft. ISAM. esent. Interop. EsentKeyBoundaryException</span><span class="sxs-lookup"><span data-stu-id="21f62-170">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>](./esentkeyboundaryexception-class.md)  
            [<span data-ttu-id="21f62-171">Microsoft. ISAM. esent. Interop. EsentKeyTooBigException</span><span class="sxs-lookup"><span data-stu-id="21f62-171">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>](./esentkeytoobigexception-class.md)  
            [<span data-ttu-id="21f62-172">Microsoft. ISAM. esent. Interop. EsentLanguageNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="21f62-172">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>](./esentlanguagenotsupportedexception-class.md)  
            [<span data-ttu-id="21f62-173">Microsoft. ISAM. esent. Interop. EsentLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="21f62-173">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>](./esentlinknotsupportedexception-class.md)  
            [<span data-ttu-id="21f62-174">Microsoft. ISAM. esent. Interop. EsentLogBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="21f62-174">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>](./esentlogbuffertoosmallexception-class.md)  
            [<span data-ttu-id="21f62-175">Microsoft. ISAM. esent. Interop. EsentMissingPatchPageException</span><span class="sxs-lookup"><span data-stu-id="21f62-175">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>](./esentmissingpatchpageexception-class.md)  
            [<span data-ttu-id="21f62-176">Microsoft. ISAM. esent. Interop. EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="21f62-176">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [<span data-ttu-id="21f62-177">Microsoft. ISAM. esent. Interop. EsentMustDisableLoggingForDbUpgradeException</span><span class="sxs-lookup"><span data-stu-id="21f62-177">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [<span data-ttu-id="21f62-178">Microsoft. ISAM. esent. Interop. EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="21f62-178">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>](./esentnotindistributedtransactionexception-class.md)  
            [<span data-ttu-id="21f62-179">Microsoft. ISAM. esent. Interop. EsentObjectDuplicateException</span><span class="sxs-lookup"><span data-stu-id="21f62-179">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>](./esentobjectduplicateexception-class.md)  
            [<span data-ttu-id="21f62-180">Microsoft. ISAM. esent. Interop. EsentPageBoundaryException</span><span class="sxs-lookup"><span data-stu-id="21f62-180">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>](./esentpageboundaryexception-class.md)  
            [<span data-ttu-id="21f62-181">Microsoft. ISAM. esent. Interop. EsentPatchFileMissingException</span><span class="sxs-lookup"><span data-stu-id="21f62-181">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>](./esentpatchfilemissingexception-class.md)  
            [<span data-ttu-id="21f62-182">Microsoft. ISAM. esent. Interop. EsentRfsFailureException</span><span class="sxs-lookup"><span data-stu-id="21f62-182">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>](./esentrfsfailureexception-class.md)  
            [<span data-ttu-id="21f62-183">Microsoft. ISAM. esent. Interop. EsentRfsNotArmedException</span><span class="sxs-lookup"><span data-stu-id="21f62-183">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>](./esentrfsnotarmedexception-class.md)  
            [<span data-ttu-id="21f62-184">Microsoft. ISAM. esent. Interop. EsentRollbackRequiredException</span><span class="sxs-lookup"><span data-stu-id="21f62-184">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>](./esentrollbackrequiredexception-class.md)  
            [<span data-ttu-id="21f62-185">Microsoft. ISAM. esent. Interop. EsentSLVBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="21f62-185">Microsoft.Isam.Esent.Interop.EsentSLVBufferTooSmallException</span></span>](./esentslvbuffertoosmallexception-class.md)  
            [<span data-ttu-id="21f62-186">Microsoft. ISAM. esent. Interop. EsentSLVColumnCannotDeleteException</span><span class="sxs-lookup"><span data-stu-id="21f62-186">Microsoft.Isam.Esent.Interop.EsentSLVColumnCannotDeleteException</span></span>](./esentslvcolumncannotdeleteexception-class.md)  
            [<span data-ttu-id="21f62-187">Microsoft. ISAM. esent. Interop. EsentSLVColumnDefaultValueNotAllowedException</span><span class="sxs-lookup"><span data-stu-id="21f62-187">Microsoft.Isam.Esent.Interop.EsentSLVColumnDefaultValueNotAllowedException</span></span>](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [<span data-ttu-id="21f62-188">Microsoft. ISAM. esent. Interop. EsentSLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="21f62-188">Microsoft.Isam.Esent.Interop.EsentSLVCorruptedException</span></span>](./esentslvcorruptedexception-class.md)  
            [<span data-ttu-id="21f62-189">Microsoft. ISAM. esent. Interop. EsentSLVDatabaseMissingException</span><span class="sxs-lookup"><span data-stu-id="21f62-189">Microsoft.Isam.Esent.Interop.EsentSLVDatabaseMissingException</span></span>](./esentslvdatabasemissingexception-class.md)  
            [<span data-ttu-id="21f62-190">Microsoft. ISAM. esent. Interop. EsentSLVEAListCorruptException</span><span class="sxs-lookup"><span data-stu-id="21f62-190">Microsoft.Isam.Esent.Interop.EsentSLVEAListCorruptException</span></span>](./esentslvealistcorruptexception-class.md)  
            [<span data-ttu-id="21f62-191">Microsoft. ISAM. esent. Interop. EsentSLVEAListTooBigException</span><span class="sxs-lookup"><span data-stu-id="21f62-191">Microsoft.Isam.Esent.Interop.EsentSLVEAListTooBigException</span></span>](./esentslvealisttoobigexception-class.md)  
            [<span data-ttu-id="21f62-192">Microsoft. ISAM. esent. Interop. EsentSLVEAListZeroAllocationException</span><span class="sxs-lookup"><span data-stu-id="21f62-192">Microsoft.Isam.Esent.Interop.EsentSLVEAListZeroAllocationException</span></span>](./esentslvealistzeroallocationexception-class.md)  
            [<span data-ttu-id="21f62-193">Microsoft. ISAM. esent. Interop. EsentSLVFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="21f62-193">Microsoft.Isam.Esent.Interop.EsentSLVFileAccessDeniedException</span></span>](./esentslvfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="21f62-194">Microsoft. ISAM. esent. Interop. EsentSLVFileInUseException</span><span class="sxs-lookup"><span data-stu-id="21f62-194">Microsoft.Isam.Esent.Interop.EsentSLVFileInUseException</span></span>](./esentslvfileinuseexception-class.md)  
            [<span data-ttu-id="21f62-195">Microsoft. ISAM. esent. Interop. EsentSLVFileInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="21f62-195">Microsoft.Isam.Esent.Interop.EsentSLVFileInvalidPathException</span></span>](./esentslvfileinvalidpathexception-class.md)  
            [<span data-ttu-id="21f62-196">Microsoft. ISAM. esent. Interop. EsentSLVFileIOException</span><span class="sxs-lookup"><span data-stu-id="21f62-196">Microsoft.Isam.Esent.Interop.EsentSLVFileIOException</span></span>](./esentslvfileioexception-class.md)  
            [<span data-ttu-id="21f62-197">Microsoft. ISAM. esent. Interop. EsentSLVFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="21f62-197">Microsoft.Isam.Esent.Interop.EsentSLVFileNotFoundException</span></span>](./esentslvfilenotfoundexception-class.md)  
            [<span data-ttu-id="21f62-198">Microsoft. ISAM. esent. Interop. EsentSLVFileStaleException</span><span class="sxs-lookup"><span data-stu-id="21f62-198">Microsoft.Isam.Esent.Interop.EsentSLVFileStaleException</span></span>](./esentslvfilestaleexception-class.md)  
            [<span data-ttu-id="21f62-199">Microsoft. ISAM. esent. Interop. EsentSLVFileUnknownException</span><span class="sxs-lookup"><span data-stu-id="21f62-199">Microsoft.Isam.Esent.Interop.EsentSLVFileUnknownException</span></span>](./esentslvfileunknownexception-class.md)  
            [<span data-ttu-id="21f62-200">Microsoft. ISAM. esent. Interop. EsentSLVHeaderBadChecksumException</span><span class="sxs-lookup"><span data-stu-id="21f62-200">Microsoft.Isam.Esent.Interop.EsentSLVHeaderBadChecksumException</span></span>](./esentslvheaderbadchecksumexception-class.md)  
            [<span data-ttu-id="21f62-201">Microsoft. ISAM. esent. Interop. EsentSLVHeaderCorruptedException</span><span class="sxs-lookup"><span data-stu-id="21f62-201">Microsoft.Isam.Esent.Interop.EsentSLVHeaderCorruptedException</span></span>](./esentslvheadercorruptedexception-class.md)  
            [<span data-ttu-id="21f62-202">Microsoft. ISAM. esent. Interop. EsentSLVInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="21f62-202">Microsoft.Isam.Esent.Interop.EsentSLVInvalidPathException</span></span>](./esentslvinvalidpathexception-class.md)  
            [<span data-ttu-id="21f62-203">Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapAlreadyExistsException</span><span class="sxs-lookup"><span data-stu-id="21f62-203">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapAlreadyExistsException</span></span>](./esentslvownermapalreadyexistsexception-class.md)  
            [<span data-ttu-id="21f62-204">Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapCorruptedException</span><span class="sxs-lookup"><span data-stu-id="21f62-204">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapCorruptedException</span></span>](./esentslvownermapcorruptedexception-class.md)  
            [<span data-ttu-id="21f62-205">Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapPageNotFoundException</span><span class="sxs-lookup"><span data-stu-id="21f62-205">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapPageNotFoundException</span></span>](./esentslvownermappagenotfoundexception-class.md)  
            [<span data-ttu-id="21f62-206">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotCommittedException</span><span class="sxs-lookup"><span data-stu-id="21f62-206">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotCommittedException</span></span>](./esentslvpagesnotcommittedexception-class.md)  
            [<span data-ttu-id="21f62-207">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="21f62-207">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotDeletedException</span></span>](./esentslvpagesnotdeletedexception-class.md)  
            [<span data-ttu-id="21f62-208">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotFreeException</span><span class="sxs-lookup"><span data-stu-id="21f62-208">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotFreeException</span></span>](./esentslvpagesnotfreeexception-class.md)  
            [<span data-ttu-id="21f62-209">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotReservedException</span><span class="sxs-lookup"><span data-stu-id="21f62-209">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotReservedException</span></span>](./esentslvpagesnotreservedexception-class.md)  
            [<span data-ttu-id="21f62-210">Microsoft. ISAM. esent. Interop. EsentSLVProviderNotLoadedException</span><span class="sxs-lookup"><span data-stu-id="21f62-210">Microsoft.Isam.Esent.Interop.EsentSLVProviderNotLoadedException</span></span>](./esentslvprovidernotloadedexception-class.md)  
            [<span data-ttu-id="21f62-211">Microsoft. ISAM. esent. Interop. EsentSLVProviderVersionMismatchException</span><span class="sxs-lookup"><span data-stu-id="21f62-211">Microsoft.Isam.Esent.Interop.EsentSLVProviderVersionMismatchException</span></span>](./esentslvproviderversionmismatchexception-class.md)  
            [<span data-ttu-id="21f62-212">Microsoft. ISAM. esent. Interop. EsentSLVReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="21f62-212">Microsoft.Isam.Esent.Interop.EsentSLVReadVerifyFailureException</span></span>](./esentslvreadverifyfailureexception-class.md)  
            [<span data-ttu-id="21f62-213">Microsoft. ISAM. esent. Interop. EsentSLVRootNotSpecifiedException</span><span class="sxs-lookup"><span data-stu-id="21f62-213">Microsoft.Isam.Esent.Interop.EsentSLVRootNotSpecifiedException</span></span>](./esentslvrootnotspecifiedexception-class.md)  
            [<span data-ttu-id="21f62-214">Microsoft. ISAM. esent. Interop. EsentSLVRootPathInvalidException</span><span class="sxs-lookup"><span data-stu-id="21f62-214">Microsoft.Isam.Esent.Interop.EsentSLVRootPathInvalidException</span></span>](./esentslvrootpathinvalidexception-class.md)  
            [<span data-ttu-id="21f62-215">Microsoft. ISAM. esent. Interop. EsentSLVRootStillOpenException</span><span class="sxs-lookup"><span data-stu-id="21f62-215">Microsoft.Isam.Esent.Interop.EsentSLVRootStillOpenException</span></span>](./esentslvrootstillopenexception-class.md)  
            [<span data-ttu-id="21f62-216">Microsoft. ISAM. esent. Interop. EsentSLVSpaceCorruptedException</span><span class="sxs-lookup"><span data-stu-id="21f62-216">Microsoft.Isam.Esent.Interop.EsentSLVSpaceCorruptedException</span></span>](./esentslvspacecorruptedexception-class.md)  
            [<span data-ttu-id="21f62-217">Microsoft. ISAM. esent. Interop. EsentSLVSpaceWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="21f62-217">Microsoft.Isam.Esent.Interop.EsentSLVSpaceWriteConflictException</span></span>](./esentslvspacewriteconflictexception-class.md)  
            [<span data-ttu-id="21f62-218">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileAlreadyExistsException</span><span class="sxs-lookup"><span data-stu-id="21f62-218">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileAlreadyExistsException</span></span>](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [<span data-ttu-id="21f62-219">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileFullException</span><span class="sxs-lookup"><span data-stu-id="21f62-219">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileFullException</span></span>](./esentslvstreamingfilefullexception-class.md)  
            [<span data-ttu-id="21f62-220">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileInUseException</span><span class="sxs-lookup"><span data-stu-id="21f62-220">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileInUseException</span></span>](./esentslvstreamingfileinuseexception-class.md)  
            [<span data-ttu-id="21f62-221">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileMissingException</span><span class="sxs-lookup"><span data-stu-id="21f62-221">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileMissingException</span></span>](./esentslvstreamingfilemissingexception-class.md)  
            [<span data-ttu-id="21f62-222">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileNotCreatedException</span><span class="sxs-lookup"><span data-stu-id="21f62-222">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileNotCreatedException</span></span>](./esentslvstreamingfilenotcreatedexception-class.md)  
            [<span data-ttu-id="21f62-223">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileReadOnlyException</span><span class="sxs-lookup"><span data-stu-id="21f62-223">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileReadOnlyException</span></span>](./esentslvstreamingfilereadonlyexception-class.md)  
            [<span data-ttu-id="21f62-224">Microsoft. ISAM. esent. Interop. EsentSoftRecoveryOnSnapshotException</span><span class="sxs-lookup"><span data-stu-id="21f62-224">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException</span></span>](./esentsoftrecoveryonsnapshotexception-class.md)  
            [<span data-ttu-id="21f62-225">Microsoft. ISAM. esent. Interop. EsentSPAvailExtCacheOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="21f62-225">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>](./esentspavailextcacheoutofmemoryexception-class.md)  
            [<span data-ttu-id="21f62-226">Microsoft. ISAM. esent. Interop. EsentSPAvailExtCacheOutOfSyncException</span><span class="sxs-lookup"><span data-stu-id="21f62-226">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException</span></span>](./esentspavailextcacheoutofsyncexception-class.md)  
            [<span data-ttu-id="21f62-227">Microsoft. ISAM. esent. Interop. EsentSQLLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="21f62-227">Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException</span></span>](./esentsqllinknotsupportedexception-class.md)  
            [<span data-ttu-id="21f62-228">Microsoft. ISAM. esent. Interop. EsentStreamingDataNotLoggedException</span><span class="sxs-lookup"><span data-stu-id="21f62-228">Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException</span></span>](./esentstreamingdatanotloggedexception-class.md)  
            [<span data-ttu-id="21f62-229">Microsoft. ISAM. esent. Interop. EsentTaggedNotNULLException</span><span class="sxs-lookup"><span data-stu-id="21f62-229">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>](./esenttaggednotnullexception-class.md)  
            [<span data-ttu-id="21f62-230">Microsoft. ISAM. esent. Interop. EsentTempFileOpenErrorException</span><span class="sxs-lookup"><span data-stu-id="21f62-230">Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException</span></span>](./esenttempfileopenerrorexception-class.md)  
            [<span data-ttu-id="21f62-231">Microsoft. ISAM. esent. Interop. EsentTooManyOpenDatabasesException</span><span class="sxs-lookup"><span data-stu-id="21f62-231">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>](./esenttoomanyopendatabasesexception-class.md)  
            [<span data-ttu-id="21f62-232">Microsoft. ISAM. esent. Interop. EsentTooManySplitsException</span><span class="sxs-lookup"><span data-stu-id="21f62-232">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>](./esenttoomanysplitsexception-class.md)  
            [<span data-ttu-id="21f62-233">Microsoft. ISAM. esent. Interop. EsentUnicodeTranslationBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="21f62-233">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationBufferTooSmallException</span></span>](./esentunicodetranslationbuffertoosmallexception-class.md)