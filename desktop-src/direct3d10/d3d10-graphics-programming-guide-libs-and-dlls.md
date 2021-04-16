---
description: Para que una aplicación se ejecute correctamente, el equipo host debe tener instalados los archivos dll adecuados. El sistema operativo o el paquete redistribuible de las aplicaciones pueden proporcionar estos archivos dll.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Vinculación de bibliotecas estáticas y dinámicas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696106"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>Vinculación de bibliotecas estáticas y dinámicas (Direct3D 10)

Para que una aplicación se ejecute correctamente, el equipo host debe tener instalados los archivos dll adecuados. El sistema operativo o el paquete redistribuible de las aplicaciones pueden proporcionar estos archivos dll.

## <a name="libraries-load-appropriate-dlls"></a>Las bibliotecas cargan los archivos dll adecuados

Las bibliotecas incluidas con el SDK de DirectX cargarán automáticamente los archivos dll adecuados en tiempo de ejecución. La excepción a esta regla es d3dx10. lib/d3dx10d. lib, que cargará el d3dx10.dll que se distribuyó con esa versión del SDK. Por ejemplo, si el SDK descargado incluye d3dx10 \_33.dll y d3dx10 \_34.dll, la biblioteca (d3dx10. lib) que se suministra con ese SDK cargará d3dx10 \_34.dll. Si se instala posteriormente un SDK posterior que contiene d3dx10 \_ 35. lib, d3dx10. lib del SDK anterior seguirá cargando d3dx10 \_34.dll. El d3dx10. lib del SDK más reciente cargará d3dx10 \_35.dll.

## <a name="redistributing-binaries"></a>Redistribuir archivos binarios

Solo se pueden redistribuir d3dx10.dll (y las versiones posteriores del mismo archivo). Para redistribuir este archivo, debe utilizar la función **DirectXSetup** . Para más información sobre el uso de esta función y la agrupación de un paquete redistribuible, consulte [instalación de DirectX con DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx). El resto de los binarios necesarios se incluyen en Windows Vista. Los únicos binarios que se pueden redistribuir son los que se encuentran en el siguiente directorio.


```
(SDK root)\Redist
```



En la tabla siguiente se describen los archivos binarios que los desarrolladores deben tener en cuenta.



| Archivos binarios de Direct3D 10   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | Componentes D3DX10 comerciales y de depuración; los componentes comerciales se pueden redistribuir en el archivo CAB de Redist.                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | Rasterizador de referencia. Proporciona la implementación de software de la canalización de gráficos. Solo se incluye como parte del SDK de DirectX Windows SDK o heredado y no se puede redistribuir. El rasterizador de referencia está pensado únicamente para la depuración. No es necesaria la vinculación explícita; Si se intenta crear un dispositivo de referencia (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)), se cargará este archivo dll si está presente.                                                                                                    |
| d3d10sdklayers.dll     | Una serie de utilidades de SDK que actúan como una capa entre las llamadas API y la ejecución en tiempo de ejecución, incluida la [capa de depuración](d3d10-graphics-programming-guide-api-features-layers.md) y la capa de cambio a referencia. No es necesaria la vinculación explícita; Si un dispositivo se crea con la marca de capa adecuada, este archivo DLL se carga automáticamente. Este componente está pensado únicamente para fines de desarrollo y depuración. Solo se incluye como parte del SDK de DirectX Windows SDK o heredado y no se puede redistribuir. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Gráficos de Direct3D 10](d3d10-graphics.md)
</dt> </dl>

 

 



