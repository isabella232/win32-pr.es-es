---
description: Extiende las propiedades definidas para las API del conjunto de filas.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706885"
---
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="62612-103">DBPROPSET \_ MSIDXS \_ ROWSETEXT</span><span class="sxs-lookup"><span data-stu-id="62612-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="62612-104">Extiende las propiedades definidas para las API del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="62612-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="62612-105">El \_ conjunto de propiedades DBPROPSET MSIDXS \_ ROWSETEXT contiene las siguientes constantes de propiedad:</span><span class="sxs-lookup"><span data-stu-id="62612-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="62612-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS</span><span class="sxs-lookup"><span data-stu-id="62612-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="62612-107">IDENTIFICADOR de propiedad 2.</span><span class="sxs-lookup"><span data-stu-id="62612-107">Property ID 2.</span></span> <span data-ttu-id="62612-108">Estado de la consulta para el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="62612-108">Query status for the rowset.</span></span> <span data-ttu-id="62612-109">Las constantes de STAT \_ \* indican la ejecución y el estado de confiabilidad.</span><span class="sxs-lookup"><span data-stu-id="62612-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="62612-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_cadena de \_ configuración regional del comando MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="62612-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="62612-111">IDENTIFICADOR de propiedad 3.</span><span class="sxs-lookup"><span data-stu-id="62612-111">Property ID 3.</span></span> <span data-ttu-id="62612-112">Cadena de configuración regional que representa la configuración regional y de idioma que se va a usar para este conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="62612-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="62612-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_restricción de consulta MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="62612-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="62612-114">IDENTIFICADOR de propiedad 4.</span><span class="sxs-lookup"><span data-stu-id="62612-114">Property ID 4.</span></span> <span data-ttu-id="62612-115">Cadena de consulta asociada a este conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="62612-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="62612-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_árbol de análisis de MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="62612-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="62612-117">IDENTIFICADOR de propiedad 5.</span><span class="sxs-lookup"><span data-stu-id="62612-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="62612-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_rango máximo de MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="62612-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="62612-119">IDENTIFICADOR de propiedad 6.</span><span class="sxs-lookup"><span data-stu-id="62612-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="62612-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>resultados de MSIDXSPROP \_ \_ encontrados</span><span class="sxs-lookup"><span data-stu-id="62612-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="62612-121">IDENTIFICADOR de propiedad 7.</span><span class="sxs-lookup"><span data-stu-id="62612-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="62612-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID</span><span class="sxs-lookup"><span data-stu-id="62612-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="62612-123">IDENTIFICADOR de propiedad 8.</span><span class="sxs-lookup"><span data-stu-id="62612-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="62612-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_versión del servidor de MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="62612-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="62612-125">Novedades de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62612-125">New for Windows 7.</span></span> <span data-ttu-id="62612-126">IDENTIFICADOR de propiedad 9.</span><span class="sxs-lookup"><span data-stu-id="62612-126">Property ID 9.</span></span> <span data-ttu-id="62612-127">La versión del servidor.</span><span class="sxs-lookup"><span data-stu-id="62612-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="62612-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ Server \_ winver \_ major</span><span class="sxs-lookup"><span data-stu-id="62612-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="62612-129">IDENTIFICADOR de propiedad 10.</span><span class="sxs-lookup"><span data-stu-id="62612-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="62612-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ Server \_ winver \_ Minor</span><span class="sxs-lookup"><span data-stu-id="62612-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="62612-131">IDENTIFICADOR de propiedad 11.</span><span class="sxs-lookup"><span data-stu-id="62612-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="62612-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ Server \_ NLSVERSION</span><span class="sxs-lookup"><span data-stu-id="62612-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="62612-133">IDENTIFICADOR de propiedad 12.</span><span class="sxs-lookup"><span data-stu-id="62612-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="62612-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ Server \_ NLSVER \_ DEFINED</span><span class="sxs-lookup"><span data-stu-id="62612-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="62612-135">IDENTIFICADOR de propiedad 13.</span><span class="sxs-lookup"><span data-stu-id="62612-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="62612-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ mismo \_ orden \_ usado</span><span class="sxs-lookup"><span data-stu-id="62612-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="62612-137">IDENTIFICADOR de propiedad 14.</span><span class="sxs-lookup"><span data-stu-id="62612-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62612-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62612-138">Remarks</span></span>

<span data-ttu-id="62612-139">Para consultar la \_ versión del servidor de MSIDXSPROP \_ , es necesario emitir la consulta ficticia en el servidor, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="62612-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="62612-140">Una vez devuelto el conjunto de filas, llame a [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener las capacidades del conjunto de filas y, a continuación, llame a [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) para la nueva propiedad (MSIDXSPROP \_ Server \_ version).</span><span class="sxs-lookup"><span data-stu-id="62612-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="62612-141">La propiedad tiene un tipo de **VT \_ I4** y puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="62612-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="62612-142">\#definir la \_ versión de CI \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="62612-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="62612-143">\#definir la \_ versión de CI \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="62612-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="62612-144">\#definir la \_ versión de CI \_ WIN70 0x700//1792</span><span class="sxs-lookup"><span data-stu-id="62612-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="62612-145">Una vez que se conoce el valor, el cliente puede crear una consulta que sea compatible con el servidor y emitir una consulta real.</span><span class="sxs-lookup"><span data-stu-id="62612-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="62612-146">DBPROPSET \_ MSIDXS \_ ROWSETEXT se declara en NTQuery. h.</span><span class="sxs-lookup"><span data-stu-id="62612-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
