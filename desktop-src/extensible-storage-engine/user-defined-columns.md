---
description: 'Más información sobre: columnas definidas por el usuario'
title: Columnas definidas por el usuario
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082375"
---
# <a name="user-defined-columns"></a><span data-ttu-id="bdf86-103">Columnas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="bdf86-103">User Defined Columns</span></span>


<span data-ttu-id="bdf86-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bdf86-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="bdf86-105">Columnas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="bdf86-105">User Defined Columns</span></span>

<span data-ttu-id="bdf86-106">Las columnas definidas por el usuario son columnas cuyos valores predeterminados se proporcionan mediante una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bdf86-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="bdf86-107">Estas columnas siempre se etiquetan y se establecen en el valor calculado por la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bdf86-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="bdf86-108">Este valor debe ser estable para cada fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bdf86-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="bdf86-109">La función de devolución de llamada solo se usa cuando la aplicación o el motor de base de datos debe leer el valor de la columna de una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="bdf86-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="bdf86-110">La aplicación tiene la opción de invalidar el valor predeterminado y establecer un valor específico en la columna.</span><span class="sxs-lookup"><span data-stu-id="bdf86-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="bdf86-111">Cuando se invalida el valor predeterminado en las columnas, utiliza el espacio de la fila; de lo contrario, las columnas predeterminadas definidas por el usuario no usan espacio en el registro.</span><span class="sxs-lookup"><span data-stu-id="bdf86-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="bdf86-112">La opción valores predeterminados definidos por el usuario se establece en el miembro **grbit** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) en la llamada a [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="bdf86-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="bdf86-113">El parámetro *pvDefault* de la función [JetAddColumn](./jetaddcolumn-function.md) apunta a una estructura [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , que contiene el nombre de la función de devolución de llamada en el miembro **szCallback** , y los datos que se pasan a la devolución de llamada en el miembro **pbUserData** .</span><span class="sxs-lookup"><span data-stu-id="bdf86-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
