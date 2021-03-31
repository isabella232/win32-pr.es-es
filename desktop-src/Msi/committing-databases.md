---
description: Los cambios realizados en la base de datos de instalación no se escriben en la base de datos hasta que se llama a MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Confirmar bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911342"
---
# <a name="committing-databases"></a><span data-ttu-id="50047-103">Confirmar bases de datos</span><span class="sxs-lookup"><span data-stu-id="50047-103">Committing Databases</span></span>

<span data-ttu-id="50047-104">Los cambios realizados en la base de datos de instalación no se escriben en la base de datos hasta que se llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="50047-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="50047-105">**Para asegurarse de que se finalizan los cambios realizados en una base de datos**</span><span class="sxs-lookup"><span data-stu-id="50047-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="50047-106">Compruebe si una tabla se escribirá al llamar a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) llamando a [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span><span class="sxs-lookup"><span data-stu-id="50047-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="50047-107">Llame a la función [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) para finalizar los cambios en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="50047-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="50047-108">Los cambios realizados en una base de datos se acumulan y no se reflejan en la base de datos real hasta que se llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="50047-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="50047-109">Las columnas o filas temporales no se confirman en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="50047-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="50047-110">Cuando se cierra una base de datos, se revierten automáticamente todos los cambios realizados desde el último **MsiDatabaseCommit** .</span><span class="sxs-lookup"><span data-stu-id="50047-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



