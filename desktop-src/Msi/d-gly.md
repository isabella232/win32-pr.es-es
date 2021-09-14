---
description: Obtenga información sobre Windows installer que comienzan por la letra D, como la función de base de datos y la revisión diferencial.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158658"
---
# <a name="d-windows-installer"></a>D (Windows instalador)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) G [H](g-gly.md) [I](i-gly.md) J K L M [N](m-gly.md) [O](o-gly.md) P [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**función de base de datos**
</dt> <dd>

Accede a la base de datos del instalador. Estas funciones se proporcionan principalmente [](i-gly.md) para su uso por las herramientas de creación de paquetes del instalador y no están diseñadas para usarse para llamar a los servicios del instalador. Para obtener más información, vea [Funciones de base de datos](database-functions.md) y la Referencia de función del [instalador](installer-function-reference.md).

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**identificador de base de datos**
</dt> <dd>

Necesario para trabajar con una base de datos. Para obtener más información, vea [Obtener un identificador de base de datos](obtaining-a-database-handle.md).

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**revisión delta**
</dt> <dd>

Una revisión diferencial es una revisión del instalador Windows delta creada mediante una herramienta, como Patchwiz.dll, que admite la compresión diferencial. Las revisiones que usan la compresión diferencial pueden reducir el tamaño de una actualización proporcionando solo las diferencias (deltas) entre los archivos existentes en un equipo de destino y los nuevos archivos deseados. Los nuevos archivos deseados se sintetizan a partir de los archivos existentes y las diferencias descargadas. Para obtener más información sobre la tecnología de compresión diferencial, vea La interfaz de programación [de aplicaciones de compresión diferencial](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



