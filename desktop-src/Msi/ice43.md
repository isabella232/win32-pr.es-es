---
description: ICE43 valida que los métodos abreviados que no hacen referencia a una característica como su destino (métodos abreviados no anunciados) se encuentran en componentes con una entrada de registro HKCU como su ruta de acceso de clave.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156716"
---
# <a name="ice43"></a>ICE43

ICE43 valida que los métodos abreviados que no hacen referencia a una característica como su destino (métodos abreviados no anunciados) se encuentran en componentes con una entrada de registro HKCU como su ruta de acceso de clave.

## <a name="result"></a>Resultado

ICE43 envía un mensaje de error si un método abreviado no anunciado está en un componente que no tiene una entrada de registro HKCU como ruta de acceso de la clave.

## <a name="example"></a>Ejemplo

ICE43 notificaría los siguientes errores para el ejemplo que se muestra.



| Error ICE43                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El componente Component1 tiene accesos directos no anunciados. Debe usar una clave del registro en HKCU como su ruta de acceso, no un archivo.                    | La columna Attributes de Component1 es 0, lo que significa que el componente utiliza un archivo como su ruta de acceso. Esto hace que los accesos directos no anunciados de este componente se instalen solo para el primer usuario del equipo. Los usuarios que instalen el componente más adelante no verán los métodos abreviados porque el componente aparecerá en el instalador como ya existe en el equipo. Para corregir este error, establezca el bit RegistryKeyPath de los atributos para cambiar el componente a una entrada del registro y, a continuación, cambie el valor de la ruta de acceso a una entrada válida en la tabla del registro.<br/> |
| El componente Component2 tiene accesos directos no anunciados. Debe usar una clave del registro en HKCU como su ruta de clave. La ruta de la ruta de la ruta es actualmente null. | La columna Attributes está establecida para usar el registro, pero la ruta de clave es NULL. La ruta de acceso clave debe hacer referencia a una entrada de la tabla del registro. Para corregir este error, cambie el valor de la ruta de acceso a una entrada válida en la tabla del registro.<br/>                                                                                                                                                                                                                                                                                                                               |
| El componente Component3 tiene accesos directos no anunciados. La clave del registro de la ruta de claves debe estar en HKCU.                                       | La columna Attributes está establecida para usar el registro, pero la entrada del registro a la que se hace referencia no está en HKCU. Para corregir este error, cambie a una entrada del registro diferente como la ruta de acceso de este componente o cambie el valor raíz de la entrada del registro a-1 o 1.<br/>                                                                                                                                                                                                                                                                             |
| La entrada del registro de la ruta de acceso del componente Component4 no existe.                                                                     | La entrada del registro a la que se hace referencia en la columna de ruta de clave del componente no se encuentra en la tabla del registro. Para corregir este error, cree una entrada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La entrada del registro Reg5 se establece como la ruta de acceso clave para el componente Component5, pero esa entrada del registro no pertenece a Component5.          | Hay una entrada de registro a la que se hace referencia en la columna de clave de ruta de acceso del componente que se encuentra bajo el árbol HKCU, pero la columna de componente de la entrada del registro \_ no hace referencia al mismo componente que la ha mostrado como ruta de acceso clave. Esto significa que la entrada del registro utilizada como ruta de acceso del componente solo se crea si se ha instalado algún otro componente. Para corregir este error, cambie el valor de la ruta de acceso para hacer referencia a una entrada del registro que pertenezca al componente o cambie la entrada del registro para que pertenezca al componente que lo usa como una ruta de acceso clave.<br/>   |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributos | Rutas |
|------------|------------|---------|
| Component1 | 0          | Archivo1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Component4 | 4          | Reg4    |
| Component5 | 4          | Reg5    |



 

[Tabla del registro](registry-table.md) (parcial)



| Registro | Root | Value | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




