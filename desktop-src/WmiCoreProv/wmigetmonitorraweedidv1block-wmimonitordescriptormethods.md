---
description: Obtiene los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de vídeo electrónica estándar (VESA) que define los valores óptimos para configurar un monitor.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Método WmiGetMonitorRawEEdidV1Block de la clase WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706941"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="71a37-103">Método WmiGetMonitorRawEEdidV1Block de la clase WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="71a37-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="71a37-104">El método **WmiGetMonitorRawEEdidV1Block** obtiene los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de vídeo electrónica de vídeo (VESA) que define la configuración óptima para la configuración de un monitor.</span><span class="sxs-lookup"><span data-stu-id="71a37-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71a37-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="71a37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71a37-107">*BlockId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71a37-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a37-108">La identidad del bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="71a37-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="71a37-109">*BlockType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71a37-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71a37-110">Tipo de bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="71a37-110">Type of data block.</span></span> <span data-ttu-id="71a37-111">En la tabla siguiente se enumeran los posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="71a37-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="71a37-112">Value</span><span class="sxs-lookup"><span data-stu-id="71a37-112">Value</span></span>                                                                                 | <span data-ttu-id="71a37-113">Significado</span><span class="sxs-lookup"><span data-stu-id="71a37-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="71a37-114"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="71a37-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="71a37-115">No inicializado</span><span class="sxs-lookup"><span data-stu-id="71a37-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="71a37-116"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="71a37-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="71a37-117">Bloque base EDID</span><span class="sxs-lookup"><span data-stu-id="71a37-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="71a37-118"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="71a37-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="71a37-119">Asignación de bloques EDID</span><span class="sxs-lookup"><span data-stu-id="71a37-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="71a37-120"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="71a37-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="71a37-121">Otros</span><span class="sxs-lookup"><span data-stu-id="71a37-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="71a37-122">*BlockContent* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71a37-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71a37-123">Una matriz de 128 bytes que contiene el contenido del bloque sin formato.</span><span class="sxs-lookup"><span data-stu-id="71a37-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71a37-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71a37-124">Return value</span></span>

<span data-ttu-id="71a37-125">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="71a37-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="71a37-126">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="71a37-126">Any other number indicates an error.</span></span> <span data-ttu-id="71a37-127">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="71a37-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="71a37-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71a37-128">Examples</span></span>

<span data-ttu-id="71a37-129">En el ejemplo de código siguiente se recuperan los bloques EDID de cualquier pantalla como matrices de 128 bits sin formato.</span><span class="sxs-lookup"><span data-stu-id="71a37-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="71a37-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a37-130">Requirements</span></span>



| <span data-ttu-id="71a37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a37-131">Requirement</span></span> | <span data-ttu-id="71a37-132">Value</span><span class="sxs-lookup"><span data-stu-id="71a37-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71a37-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71a37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="71a37-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71a37-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="71a37-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71a37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="71a37-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71a37-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="71a37-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71a37-137">Namespace</span></span><br/>                | <span data-ttu-id="71a37-138">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="71a37-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="71a37-139">MOF</span><span class="sxs-lookup"><span data-stu-id="71a37-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71a37-140"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71a37-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="71a37-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71a37-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71a37-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a37-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a37-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="71a37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a37-144">**WmiMonitorDescriptorMethods**</span><span class="sxs-lookup"><span data-stu-id="71a37-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="71a37-145">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="71a37-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

