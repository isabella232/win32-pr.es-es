---
title: /n (modificador)
description: El modificador/n especifica la profundidad de composición para crear archivos de metadatos.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n cambiar MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690824"
---
# <a name="n-switch"></a>/n (modificador)

El modificador **/n** especifica la profundidad de composición para crear archivos de metadatos.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*profundidad del espacio de nombres \_* 
</dt> <dd>

Especifica la profundidad del espacio de nombres que se va a componer en un único archivo de metadatos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos son los posibles formatos de valores que puede especificar con el modificador **/n** .



| Formato del valor                   | Descripción                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Cree todos los tipos en la profundidad de espacio de nombres especificada en el modificador.               |
| -1                             | Cree todos los tipos en un archivo IDL por espacio de nombres.                              |
| <namespace>: Int32 > 0 | Cree todos los tipos con el espacio de nombres coincidente a la profundidad especificada en el modificador. |
| <namespace>:-1           | Cree todos los tipos con espacio de nombres coincidente en un archivo por espacio de nombres.          |



 

En la tabla siguiente se muestran los resultados de distintas combinaciones del modificador **/n** que funcionan en estos espacios de nombres.

-   Windows. Foundation. Collections. IIterable
-   Windows. UI. DirectUI. Controls. Button
-   Windows. UI. DirectUI. Controls. ListView
-   Windows. UI. inmersivo. Application. Playto. Target
-   Windows. Web. Syndication. RSS



| Conmutadores                         | Resultado                                                                                                                                                                                                                                                       | Explicación                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | El último modificador/n invalida todos los modificadores-n anteriores.                                                                                                                                                                                                                                                                           |
| **/n:-1/n: Windows. UI: 2**         | <dl> Windows. <dt>Foundation. winmd</dt> <dt>Windows. UI. Winmd</dt> <dt>Windows. Web. Syndication. winmd</dt> </dl> | <dl> <dt>**Windows. Foundation** siempre se compone de – n:2.</dt> <dt>Los tipos de **Windows. UI** están agrupados.</dt> <dt>**Windows. Web. Syndication** se compone de n:-1.</dt> </dl>       |
| **/n: 1/n: Windows. UI. DirectUI: 3** | <dl> Windows. <dt>Foundation. winmd</dt> <dt>Windows. UI. DirectUI. winmd</dt> <dt>Windows. winmd</dt> </dl>       | <dl> <dt>**Windows. Foundation** siempre se compone de – n:2.</dt> <dt>**Windows. UI. DirectUI** se compone en el nivel 3.</dt> <dt>Todos los demás tipos se componen en el nivel 1.</dt> </dl> |



 

Estas son las reglas para administrar varias instancias del modificador **/n** .

-   Prevalece la instancia más específica. Por ejemplo, si especifica **– n:A.B.C: 4 – n:A.B: 5**, MDMERGE resuelve a.b.c. D en el nivel 4, ya que a. B. C es más específico que A.B. A. B. E. F se resuelve en la profundidad 5, porque coincide con A. B pero no A.B.C.
-   Prevalece la última instancia. Por ejemplo, si especifica **– n:5 – n:2**, los tipos se componen en el nivel 2.
-   Ambas reglas se aplican. Si especifica – n:A.B.C: 4 – n:A.B.C: 1, el espacio de nombres A. B. C se compone en el nivel 1.

## <a name="examples"></a>Ejemplos

**mdmerge.exe-Metadata \_ dir $ ( \_ ruta de metadatos del SDK \_ )-i $ ( \_ \_ ruta de acceso de metadatos del SDK interno \_ )-o $ (obj \_ path) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation: 2**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------|
| Remoto<br/> | Windows 8<br/>           |
| Servidor<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





