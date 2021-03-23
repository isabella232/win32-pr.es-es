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
# <a name="using-the-directml-debug-layer"></a>Usar la capa de depuración DirectML

La capa de depuración DirectML es un componente opcional en tiempo de desarrollo que le ayuda a depurar el código de DirectML. La capa de depuración forma parte de un paquete independiente de herramientas de gráficos, distribuido como una [característica a petición](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (du). Los du de herramientas de gráficos deben estar instalados en el sistema para poder usar la capa de depuración.

Le recomendamos encarecidamente que habilite el nivel de depuración al desarrollar aplicaciones mediante DirectML, ya que puede proporcionar información valiosa en caso de que el uso de la API no sea válido.

## <a name="installing-the-directml-debug-layer"></a>Instalación de la capa de depuración DirectML

Para instalar el paquete opcional de características a petición (du) de herramientas de gráficos, ejecute el siguiente comando desde un símbolo del sistema de administrador de PowerShell.

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

Como alternativa, puede instalar el paquete de herramientas de gráficos desde la configuración de Windows 10. Vaya a **configuración**  >  **aplicaciones** aplicaciones  >  **& características**  >  **características opcionales**  >  **Agregar una característica** > después seleccione **herramientas de gráficos**.

## <a name="enabling-the-directml-debug-layer"></a>Habilitar la capa de depuración DirectML

Una vez instalado el paquete de herramientas de gráficos, puede habilitar la capa de depuración DirectML proporcionando  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) al llamar a [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).

> [!IMPORTANT]
> Primero debe habilitar la capa de depuración de Direct3D 12. Y *, a continuación,* habilite la capa de depuración DirectML llamando a **DMLCreateDevice**.

Una vez que haya habilitado la capa de depuración DirectML, cualquier error de DirectML o llamada API no válida hará que la información de depuración se emita como salida de depuración. A continuación se muestra un ejemplo.

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>Consulte también

* [DMLCreateDevice función)](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [Características disponibles a petición](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [Usar la validación basada en GPU con la capa de depuración de Direct3D 12](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Referencia de la capa de depuración de Direct3D 12](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
