---
title: Usar la capa de depuración DirectML
description: La capa de depuración DirectML es un componente opcional en tiempo de desarrollo que le ayuda a depurar el código de DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104549117"
---
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="f596a-103">Usar la capa de depuración DirectML</span><span class="sxs-lookup"><span data-stu-id="f596a-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="f596a-104">La capa de depuración DirectML es un componente opcional en tiempo de desarrollo que le ayuda a depurar el código de DirectML.</span><span class="sxs-lookup"><span data-stu-id="f596a-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="f596a-105">La capa de depuración forma parte de un paquete independiente de herramientas de gráficos, distribuido como una [característica a petición](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (du).</span><span class="sxs-lookup"><span data-stu-id="f596a-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="f596a-106">Los du de herramientas de gráficos deben estar instalados en el sistema para poder usar la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="f596a-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="f596a-107">Le recomendamos encarecidamente que habilite el nivel de depuración al desarrollar aplicaciones mediante DirectML, ya que puede proporcionar información valiosa en caso de que el uso de la API no sea válido.</span><span class="sxs-lookup"><span data-stu-id="f596a-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="f596a-108">Instalación de la capa de depuración DirectML</span><span class="sxs-lookup"><span data-stu-id="f596a-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="f596a-109">Para instalar el paquete opcional de características a petición (du) de herramientas de gráficos, ejecute el siguiente comando desde un símbolo del sistema de administrador de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f596a-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="f596a-110">Como alternativa, puede instalar el paquete de herramientas de gráficos desde la configuración de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f596a-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="f596a-111">Vaya a **configuración**  >  **aplicaciones** aplicaciones  >  **& características**  >  **características opcionales**  >  **Agregar una característica** > después seleccione **herramientas de gráficos**.</span><span class="sxs-lookup"><span data-stu-id="f596a-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="f596a-112">Habilitar la capa de depuración DirectML</span><span class="sxs-lookup"><span data-stu-id="f596a-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="f596a-113">Una vez instalado el paquete de herramientas de gráficos, puede habilitar la capa de depuración DirectML proporcionando  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) al llamar a [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span><span class="sxs-lookup"><span data-stu-id="f596a-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f596a-114">Primero debe habilitar la capa de depuración de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="f596a-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="f596a-115">Y *, a continuación,* habilite la capa de depuración DirectML llamando a **DMLCreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="f596a-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="f596a-116">Una vez que haya habilitado la capa de depuración DirectML, cualquier error de DirectML o llamada API no válida hará que la información de depuración se emita como salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="f596a-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="f596a-117">A continuación se muestra un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f596a-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="f596a-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f596a-118">See also</span></span>

* [<span data-ttu-id="f596a-119">DMLCreateDevice función)</span><span class="sxs-lookup"><span data-stu-id="f596a-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="f596a-120">Características disponibles a petición</span><span class="sxs-lookup"><span data-stu-id="f596a-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="f596a-121">Usar la validación basada en GPU con la capa de depuración de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f596a-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="f596a-122">Referencia de la capa de depuración de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f596a-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
