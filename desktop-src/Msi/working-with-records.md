---
description: El instalador proporciona funciones que manipulan los registros en una base de datos de instalación. Estas funciones se pueden usar junto con las funciones descritas en trabajar con consultas para realizar cambios reales en una base de datos.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Trabajar con registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652775"
---
# <a name="working-with-records"></a><span data-ttu-id="e5d7d-104">Trabajar con registros</span><span class="sxs-lookup"><span data-stu-id="e5d7d-104">Working with Records</span></span>

<span data-ttu-id="e5d7d-105">El instalador proporciona funciones que manipulan los registros en una base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="e5d7d-106">Estas funciones se pueden usar junto con las funciones descritas en [trabajar con consultas](working-with-queries.md) para realizar cambios reales en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="e5d7d-107">Las siguientes funciones crean o quitan registros:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="e5d7d-108">Para crear un nuevo registro para una base de datos, llame a la función [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="e5d7d-109">Para borrar los datos de un registro, establezca cada campo en Null llamando a la función [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="e5d7d-110">Las siguientes funciones rellenan los campos de registros especificados:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="e5d7d-111">Para establecer un registro en un entero, llame a la función [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="e5d7d-112">Para establecer un registro en una cadena, llame a la función [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="e5d7d-113">Para insertar un archivo completo en un campo de flujo, llame a la función [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="e5d7d-114">Las siguientes funciones leen valores de los campos de registros especificados:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="e5d7d-115">Para leer un valor entero de un campo, llame a la función [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="e5d7d-116">Para recuperar un valor de cadena, llame a la función [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="e5d7d-117">Para obtener un flujo, llame a la función [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="e5d7d-118">Para determinar si un campo concreto de un registro es null, llame a la función [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="e5d7d-119">Las siguientes funciones son funciones de registros informativos:</span><span class="sxs-lookup"><span data-stu-id="e5d7d-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="e5d7d-120">Para obtener el número de campos que contiene un registro, llame a la función [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="e5d7d-121">Para obtener el tamaño de un campo, llame a la función [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) .</span><span class="sxs-lookup"><span data-stu-id="e5d7d-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="e5d7d-122">El valor devuelto de **MsiRecordDataSize** es sensible al tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="e5d7d-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



