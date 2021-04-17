---
description: 'Las consultas de datos son instrucciones WQL que solicitan instancias de clases. Para emitir una consulta de datos, las aplicaciones llaman al método IWbemServices:: ExecQuery o IWbemServices:: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Solicitar datos de instancia de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697733"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="aea4b-104">Solicitar datos de instancia de clase</span><span class="sxs-lookup"><span data-stu-id="aea4b-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="aea4b-105">Las consultas de datos son instrucciones WQL que solicitan instancias de clases.</span><span class="sxs-lookup"><span data-stu-id="aea4b-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="aea4b-106">Para emitir una consulta de datos, las aplicaciones llaman al método [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) o [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="aea4b-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="aea4b-107">Las instrucciones siguientes se utilizan para realizar consultas de datos:</span><span class="sxs-lookup"><span data-stu-id="aea4b-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="aea4b-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="aea4b-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="aea4b-109">ASSOCIATORS OF</span><span class="sxs-lookup"><span data-stu-id="aea4b-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="aea4b-110">REFERENCIAS DE</span><span class="sxs-lookup"><span data-stu-id="aea4b-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="aea4b-111">ISA</span><span class="sxs-lookup"><span data-stu-id="aea4b-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="aea4b-112">La instrucción SELECT de WQL es la instrucción de Lenguaje de consulta estructurado estándar (SQL) para recuperar información, con algunas restricciones y extensiones específicas de WQL.</span><span class="sxs-lookup"><span data-stu-id="aea4b-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="aea4b-113">Aunque la instrucción SELECT de SQL se usa normalmente en el entorno de base de datos para recuperar columnas concretas de las tablas, la instrucción SELECT de WQL se usa en WMI para recuperar instancias de una sola clase.</span><span class="sxs-lookup"><span data-stu-id="aea4b-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="aea4b-114">WQL no admite consultas en varias clases.</span><span class="sxs-lookup"><span data-stu-id="aea4b-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="aea4b-115">Los asociados de y las referencias de las instrucciones son específicos de WQL y no forman parte de SQL estándar.</span><span class="sxs-lookup"><span data-stu-id="aea4b-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="aea4b-116">La instrucción ASSOCIATORS OF recupera todas las instancias de clase que están asociadas a una instancia de clase de origen determinada, y las referencias de recuperan todas las instancias que hacen referencia a una instancia de origen determinada.</span><span class="sxs-lookup"><span data-stu-id="aea4b-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="aea4b-117">Las asociaciones se representan mediante instancias de una [clase de asociación](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="aea4b-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



