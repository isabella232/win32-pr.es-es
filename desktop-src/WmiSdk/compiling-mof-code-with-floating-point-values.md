---
description: El compilador MOF acepta un valor de punto flotante especificado para una propiedad de punto flotante. El valor se redondea hacia arriba o hacia abajo y se almacena como un número de punto no flotante. Esta situación puede producir resultados inesperados.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilar código MOF con valores Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277935"
---
# <a name="compiling-mof-code-with-floating-point-values"></a><span data-ttu-id="77c1a-105">Compilar código MOF con valores Floating-Point</span><span class="sxs-lookup"><span data-stu-id="77c1a-105">Compiling MOF Code with Floating-Point Values</span></span>

<span data-ttu-id="77c1a-106">El compilador MOF acepta un valor de punto flotante especificado para una propiedad de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="77c1a-106">The MOF compiler accepts a floating-point value specified for a nonfloating-point property.</span></span> <span data-ttu-id="77c1a-107">El valor se redondea hacia arriba o hacia abajo y se almacena como un número de punto no flotante.</span><span class="sxs-lookup"><span data-stu-id="77c1a-107">The value is rounded up or down and stored as a nonfloating-point number.</span></span> <span data-ttu-id="77c1a-108">Esta situación puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="77c1a-108">This situation can cause some unexpected results.</span></span>

<span data-ttu-id="77c1a-109">En el siguiente ejemplo de código MOF se define una clase denominada **ABC** en un espacio de nombres denominado "Test".</span><span class="sxs-lookup"><span data-stu-id="77c1a-109">The following MOF code example defines a class called **abc** in a namespace called "Test".</span></span> <span data-ttu-id="77c1a-110">Este código MOF se compila sin errores, pero no se puede consultar el valor de punto flotante definido para la propiedad **exampleUint16** en la instancia que crea este código.</span><span class="sxs-lookup"><span data-stu-id="77c1a-110">This MOF code compiles without errors, but you cannot query for the floating-point value defined for the property **exampleUint16** in the instance this code creates.</span></span>

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

<span data-ttu-id="77c1a-111">Si emite la consulta siguiente, obtendrá un código de error que indica una consulta no válida.</span><span class="sxs-lookup"><span data-stu-id="77c1a-111">If you issue the following query, you get an error code that indicates an invalid query.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



<span data-ttu-id="77c1a-112">Sin embargo, la consulta siguiente busca la instancia indicada.</span><span class="sxs-lookup"><span data-stu-id="77c1a-112">However, the following query finds the indicated instance.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a><span data-ttu-id="77c1a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77c1a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c1a-114">Compilar archivos MOF</span><span class="sxs-lookup"><span data-stu-id="77c1a-114">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="77c1a-115">**MOFCOMP**</span><span class="sxs-lookup"><span data-stu-id="77c1a-115">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="77c1a-116">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="77c1a-116">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



