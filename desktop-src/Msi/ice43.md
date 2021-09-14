---
description: ICE43 valida que los accesos directos que no hacen referencia a una característica como destino (accesos directos no anunciados) están en componentes que tienen una entrada del Registro HKCU como ruta de acceso de clave.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074606"
---
# <a name="ice43"></a>ICE43

ICE43 valida que los accesos directos que no hacen referencia a una característica como destino (accesos directos no anunciados) están en componentes que tienen una entrada del Registro HKCU como ruta de acceso de clave.

## <a name="result"></a>Resultado

ICE43 envía un mensaje de error si un acceso directo no anunciado está en un componente que no tiene una entrada del Registro HKCU como ruta de acceso de clave.

## <a name="example"></a>Ejemplo

ICE43 notificaría los siguientes errores para el ejemplo mostrado.



| Error ICE43                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Componente 1 tiene accesos directos no anunciados. Debe usar una clave del Registro en HKCU como su KeyPath, no un archivo.                    | La columna attributes de Component1 es 0, lo que significa que el componente usa un archivo como su KeyPath. Esto hace que los accesos directos no anunciados de este componente se instalen solo para el primer usuario del equipo. Los usuarios que instalan el componente más adelante no ven los accesos directos porque el componente aparece en el instalador como ya existente en el equipo. Para corregir este error, establezca el bit RegistryKeyPath de los atributos para cambiar el componente a una entrada del Registro y, a continuación, cambie el valor de KeyPath a una entrada válida en la tabla del Registro.<br/> |
| Componente 2 tiene accesos directos no anunciados. Debe usar una clave del Registro en HKCU como su KeyPath. KeyPath es actualmente null. | La columna Atributos se establece para usar el Registro, pero KeyPath es null. KeyPath debe hacer referencia a una entrada de la tabla del Registro. Para corregir este error, cambie el valor de KeyPath a una entrada válida en la tabla Registry.<br/>                                                                                                                                                                                                                                                                                                                               |
| Componente 3 tiene accesos directos no anunciados. Su clave del Registro KeyPath debe estar en HKCU.                                       | La columna Atributos se establece para usar el Registro, pero la entrada del Registro a la que se hace referencia no está en HKCU. Para corregir este error, cambie a otra entrada del Registro como KeyPath para este componente o cambie el valor raíz de la entrada del Registro a -1 o 1.<br/>                                                                                                                                                                                                                                                                             |
| La entrada del Registro KeyPath para el componente Component4 no existe.                                                                     | La entrada del Registro a la que se hace referencia en la columna KeyPath del componente no está en la tabla del Registro. Para corregir este error, cree una entrada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La entrada del Registro Reg5 se establece como KeyPath para el componente Component5, pero esa entrada del Registro no pertenece a Component5.          | Hay una entrada del Registro a la que se hace referencia en la columna KeyPath del componente que se encuentra bajo el árbol HKCU, pero la columna Component de la entrada del Registro no hace referencia al mismo componente que la enumera como \_ KeyPath. Esto significa que la entrada del Registro utilizada como KeyPath del componente solo se crea si se instaló algún otro componente. Para corregir este error, cambie el valor de KeyPath para hacer referencia a una entrada del Registro que pertenece al componente o cambie la entrada del Registro para que pertenezca al componente que lo usa como KeyPath.<br/>   |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributos | KeyPath |
|------------|------------|---------|
| Componente1 | 0          | Archivo1   |
| Componente 2 | 4          |         |
| Componente 3 | 4          | Reg3    |
| Componente 4 | 4          | Reg4    |
| Componente5 | 4          | Reg5    |



 

[Tabla del Registro](registry-table.md) (parcial)



| Registro | Root | Value | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Componente 3  |
| Reg5     | 0    |       | Componente 4  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




